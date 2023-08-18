## Containerize nodejs application using docker
* The following project involves creading a Dockerfile to create a docker image for our nodejs app.
* It eases spinning up an image using docker-compose.
* There are separate docker-compose files for prod and dev environment.

### Dev Container
* Changes in the nodejs application reflect quickly in the containers created using docker-compose.dev file.

#### To turn up the container
```
$ docker-compose -f docker-compose.yml -f docker-compose.dev.yml  up -d
```
#### To turn down the container
```
$ docker-compose -f docker-compose.yml -f docker-compose.dev.yml  down
```

### Prod Container
* Does not reflect changes in the nodejs app after the image is created.
* It is kept light no unnecessary dependencies are installed.   
#### To turn up the container
```
$ docker-compose -f docker-compose.yml -f docker-compose.prod.yml  up -d
```
#### To turn down the container
```
$ docker-compose -f docker-compose.yml -f docker-compose.prod.yml  down
```