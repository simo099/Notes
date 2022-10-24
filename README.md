# Notes

## Windows Powershell Commands 

- winget: Microsoft Tool, which allows you to manage and install Microsoft Apps: 
  - winget search AppName (search App in msstore) 
  - winget install AppName (install App from msstore)     

- ls: shows all files in the current location

- mkdir: create a folder

- rmdir: remove a folder

- rm: remove

- cls: clear

- kill: stop a process 

- cd: move to a specific location

- h: history

- ps: gets the processes that are running

- cat: get the contents of a file

- exc.

### Git

- git --version: check Git's version

- git clone: clone a repository

- git init: create a empty repository

- git add: add new or changed files in the repository.

- git push: upload local repository content to remote repository

- git commit: catchs a moment of the project

- git pull: update the local version of repository from a remote repository

- git branch branchname: create a branch

- git checkout branchname: switch into branchname

### Docker

- docker run: create a container over the specific image 

- docker pull imagename: download an image

- --name: give a name to a container 

- -p port:port -> Open a host port to give us access to a corresponding open port inside the Docker container

- -p: password 

- -e: set enviroment variables

- -d: run command in background

- -u: username

- docker ps: shows running containers

- -h: hostname

- docker exec: runs a new command in a running container

- docker exec -it containername bash: moves you to bash shell

- docker-compose: a tool for defining and sharing containers. We can create a YAML file in which we define all the services, such as image, ports, user, password, and database

- docker-compose up -d: start up the application stack and run all in background

### MYSQL

- MYSQL_ROOT_PASSWORD:password -> set root password

- create database databasename: create a database

- create table tablename: create a table

- show databases; -> get a list of all running databases

- show tables; -> get all tables that are in a database 

- selct * from tablename; -> shows the table and its content

- drop table tablename; -> removes a table

## Run MySQL in a Docker Container

- docker pull mysql: download the latest image of mysql

- create MySQL container: 
  - docker run --name containername -p 3306:3306 -e MYSQL_ROOT_PASSWORD:password -d mysql:latest
  
### Connecting to MySQL

- docker exec -it containername bash

- mysql -u root -p

- insert the root password

### Create Database and Table

- create database mydb;

- show databases; 

- use mydb;

- create table table1(id int not null, name text, primary key(id));

- show tables;

- insert into table1 (id, name) values(1, 'Hello'); 

- insert into table1 (id, name) values(2, 'World');

- select * from table1; 
