# Docker Basics

Some interaction with the containers

## Let's run an Nginx container
### Pull and run a Niginx server
```bash
docker run -d -p 8080:80 --name webserver nginx
```
so here we are `run` an docker image name as `nginx` and giving its instance name as `webserver` and making it listening to port 8080:80, and -d from getting back our command prompt or terminal prompt back

- So if you go to https://localhost:8080 , you will see that our container is running and listening on it.

### List the running containers
```bash
docker ps
``` 
it will list the running container

### To list all the images on your machine
```bash
docker images
```
- to list all the images that are installed on your machine

###  Connect with the container or create instance 
```bash
docker container exe -it webserver bash
```
- to exit the instance
```
exit
```
### Stop the container 
```
docker stop webserver
```
will stop the running of the container

### To remove it from memory
```
docker rm webserver
``` 

### To remove image from machine
```
docker rmi nginx
```
