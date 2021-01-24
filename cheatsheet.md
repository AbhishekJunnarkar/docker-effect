# Docker Commands cheatsheet

## Docker Images

-- To run ubuntu image in interactive mode(i) with a bash terminal

$ docker run -it ubuntu bash

-- To check the steps executed

$ docker history

-- To check the dockerfile in a directory

$ vi /root/webapp-color/Dockerfile

-- Build a docker image using the Dockerfile and name it webapp-color

$ docker build -t webapp-color .

-- Run an instance of the image webapp-color and publish port 8080 on the container to 8282 on the host

$ docker run -p 8282:8080 webapp-color

-- What is the base Operating System used by the python:3.6 image?

$ Run docker run python:3.6 cat /etc/*release* command
## Docker run

-- Attached Mode example

$ docker run timer

-- Detatched Mode example

$ docker run -d timer

-- **** Jenkins setup on Docker example **** --

$ docker run jenkins/jenkins:lts

-- Find the IP of the jenkins container

$ docker inspect <container-id>

-- to go inside the docker container

$ docker exec -it <name> /bin/bash

-- To run docker based jenkins externally on browser

$ docker run -p 8090:8080 jenkins/jenkins:lts

-- In order to Save data after Jenkins docker container is stopped, 

-- an extenral volume needs to be mapped, like

$ docker run -p 8080:8080 -p 5000:5000 -v /your/home: /var/jenkins_home

## Basic Commands

$ which docker

$ docker --version

$ docker ps

$ docker ps -a

$ docker images

$ docker rmi <image-nm>

$ docker run -d <image-nm>

$ docker stop <container-id>

$ docker pull <image-nm>

-- detatched mode -> -d

-- interactive mode -> -i

-- attach again

$ docker attach <container-id>
