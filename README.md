# docker-r-studio

## Description

To allow usage of RStudio in a portable way using Docker Container

## Procedure

### Build the image

`docker login` - to authenticate
`docker build -t monahton/docker-r-studio .`

### Run Container
`docker run --rm -p 8787:8787 -e USER=myself -e PASSWORD=guest -v /c/Users/39388/Desktop/udemy/docker_containers/R_Studio_Shared:/home/myself/r-studio monahton/docker-r-studio`

### Stop container
`CTRL + CTRL`
`docker container ls`
`docker stop <docker id>`

### Push to Docker Hub
`docker push monahton/docker-r-studio`

### Save docker image locally
`docker save monahton/docker-r-studio > docker-r-studio.tar`

### Delete an image
`docker images`
`docker rmi <image_id>`

### Restore image from the local archive file
`docker load --input docker-r-studio.tar`

### View or enter into a running container from another terminal
`docker images`
`docker exec -it <image_id> bash
This will make the terminal a bash shell from which we can view the content of the image

### Save a new version of the image using Tags
`docker tag monahton/docker-r-studio monahton/docker-r-studio:Version0.9`






