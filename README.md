![docker](https://img.shields.io/badge/Docker-2CA5E0?style=for-the-badge&logo=docker&logoColor=white)
![docker-compose](https://img.shields.io/badge/Docker%20Compose-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![nginx](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)
![pglg](https://skillicons.dev/icons?i=js,php,perl,mysql)

# DockerLDE
This is a Local Development Environment similar to XAMPP/Laragon that is built using docker so that it is isolated, clean, and safe for the host system.

## Provides
1. Programming Languages : PHP, Node JS, Perl
2. Package Manager : npm, composer
3. Database : MySQL
4. Database Management : PhpMyAdmin
5. Web Server : Nginx

## Feature
Resources are limited according to each container, for example :
* Node JS and PHP use 100% CPU and 256MB RAM.
* Perl uses 50% CPU and 128MB RAM.
* MySQL database uses 100% CPU and 256MB RAM.
* phpmyadmin database processor uses 50% CPU and 128MB RAM.
* Nginx server uses 50% CPU and 128MB RAM.

## Project Tree
```
DockerLDE/
├── docker-compose.yml
├── nginx
│   └── default.conf
├── node
│   └── Dockerfile
├── php
│   └── Dockerfile
├── README.md
└── www
    └── index.php
```

## Tools
1. docker
2. docker-compose

## Setup
1. clone this repository
```
git clone https://github.com/rahmrafi/DockerLDE.git
```
2. go to project folder
```
cd DockerLDE/
```
3. run and build with docker-compose
```
sudo docker compose up -d --build
```
4. check if running correctly
```
sudo docker compose ps
```
5. check stats of each container
```
sudo docker stats
```
