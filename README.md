#Based on Docker file, Creating Image

docker build -t ubuntu:test1 .

#List Images
docker images

#Created Container Named "testcontainer" based on the Image -- Start and Run the Container
docker run -it --name testcontainer -d ubuntu:test1 /bin/bash

#List Docker Containers
docker ps

#Execute the Docker Container
docker exec -it testcontainer bash

#Uploading to Container to Docker Registry
#Tag
docker tag ubuntu:test1 my-registry1/my-repository1:latest

#Login into Docker 
docker login my-registry1

#Push into Docker Registry
docker push my-registry1/my-repository1:latest


