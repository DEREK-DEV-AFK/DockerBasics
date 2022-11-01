# Docker Volumes

## Create a volume
```
docker volume create myvol
```

## List the volumes
```
docker volume ls
```

## Run a Nginx container that will use the volume
```
docker run -d --name voltest -v myvol:/app nginx:latest
```

## Connect to the instance
```
docker exec -it voltest bash
```

## Create a file in the volume using Nano
```
apt-get update
apt-get install nano
```

## Create a file in the app folder
```
cd app
nano test.txt
```
nano text editor
```
CTRL+O // writing out
CTRL+X // exit nano
```

## Detach from instance
```
exit
```

## Stop and Remove the container
```
docker stop voltest
docker rm voltest
```

## Run it again and see if the file still exists
```
docker run -d --name voltest -v myvol:/app nginx:latest
docker exec -it voltest bash
cd app
cat test.txt
```

## Cleanup
```
docker stop voltest
docker volume rm myvol
docker rm voltest
```