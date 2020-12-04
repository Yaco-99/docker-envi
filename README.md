# docker-envi

## Installation

Docker : https://docs.docker.com/get-docker/  
Docker-compose : https://docs.docker.com/compose/install/

## Optionnal (linux)

Manage Docker as a non-root user (No sudo anymore) : https://docs.docker.com/engine/install/linux-postinstall/

## Getting started

- First of all you need to clone this repo somewhere in a ressource folder.
- Add a data and a htdocs folder.
- To make it easier for your future project add this alias to your shell : **alias project.docker="cp -r ~/YourPath/docker-envi "**
- Create a project : **project.docker name_of_the_project**
- Edit the doker-compose.yml file and change the name of all the containers (ctrl+d is your friend), you can also change the port if you want to.
- You can start coding **In the htdocs folder** create an index.php and write hello world.  
*If you want to run multiple projects at a time you need to change the port of the second project !*

## Compose it !

- In the docker-compose directory (with your shell), type **docker-compose up -d** your first compose up will download all the images so it will be longer.
*If you want to see all the log, remove the -d*
- And voila you can go to localhost:8081 for phpMyAdmin and localhost:2021/thefile.php to see your app.  
*localhost:2021 will be your index.php*

## Database

- If you want to import a database, put the .sql file in the **data** folder.
- Before the compose down make sure to export your database and put the .sql file in the **data** folder. **If you don't do it you will lose your data with the compose down**

## Compose down

- While you're done, do a **docker-compose down** to shut down and remove the containers.


