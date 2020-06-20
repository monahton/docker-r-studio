# docker-r-studio

## Description

To allow usage of RStudio in a portable way using Docker Container

## Procedure

### Build the image

`docker login` - to authenticate
`docker build -t monahton/docker-r-studio .`

### Run Container
`docker run --rm -p 8787:8787 -e USER=myself -e PASSWORD=guest -v /c/Users/39388/Desktop/udemy/docker_containers/R_Stu dio_Shared:/home/myself/r-studio monahton/docker-r-studio`

### Stop container
`CTRL + CTRL`
`docker container ls`
`docker stop <docker id>`

### Push to Docker Hub
`docker push monahton/docker-r-studio`

### save docker image locally
`docker save monahton/docker-r-studio > docker-r-studio.tar`



