# IIEC-Docker Project using Drupal
 In this project, I have created an infrastructure using drupal and mysql containers which can be launched in a single touch.

## Docker
Docker is a tool designed to make it easier to create, deploy, and run applications by using containers. Containers allow a developer to package up an application with all of the parts it needs, such as libraries and other dependencies, and deploy it as one package.

## Drupal
Drupal is a scalable, open platform for web content management and digital experiences. Drupal provides deep capabilities and endless flexibility on the web.

## MySQL 
MySQL is a relational database management system based on SQL – Structured Query Language. The application is used for a wide range of purposes, including data warehousing, e-commerce, and logging applications. 

### STEPS REQUIRED ###

 ### 1. Prerequisites ###
 I have done this project using RHEL Version 8(Red Hat Enterprise Linux)
 - Install Docker on the base os using `yum install docker -ce --nobest`. \\ --nobest installs the best suitable version of docker
 - Install docker-compose using the below cmd:
 
  ` curl –L"https://github.com/docker/compose/releases/download/1.25.4/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose `
   
   `chmod +x /usr/local/bin/docker-compose`
  
 ### 2. Starting Docker Service ###
 -   For starting a docker service type `systemctl start docker` inthe cmd.
     To see the status of it use  `systemctl status docker`
   
 ### 3. Download the required Images: ###
 To download the required images search for the corresponding image in https://hub.docker.com/
 
 - To Pull MySQL Image: 
    Use `docker pull mysql:5.7` to download the mysql version 5.7 image to use as a database server.
 - To Pull Drupal Image: 
    Use `docker pull drupal:8-apache` to download the drupal Image with apache server is preconfigured in it.

### 4. Creating docker-compose.yml###
 -   Create a directory for your project.
 -	 Create a docker-compose file uising`vim docker-compose.yml` inside the directory.
 -	 Place the code which is provided in the code section.
 
### 5. Starting  Docker-compose###
 -	To start docker compose in detach mode use  `docker-compose up -d`.
 
### 6. Running the Drupal Service ###
 - Use your web browser and open it using `http://ipaddress:portnumber` . 
  
### 7. Stop the docker-compose ###
 - Stop the container service using	` docker-compose stop`.

 ## REFERENCES ##
 ### Thanks for VIMAL DAGA Sir for creating this wonderfull playlist to begin with docker from scratch to expert. ###
 
 Youtube- (https://www.youtube.com/playlist?list=PLAi9X1uG6jZ30QGz7FZ55A27jPeY8EwkE)
 
