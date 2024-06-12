Docker simplifies the building and deployment of apps using lightweight containers.

Docker Image is lightweight, standalone, executable package that contains everything to run the app.

It's the blueprint for creating the containers. Containers is where the actual application runs.

Commands

* Build an image with tag
docker build -t ImageName:TagName .
    Here, . means find the Dockerfile in current directory

* List images
docker image ls

* Run a container
docker run -d -p dockerPort:appPort --name ContainerName ImageName
    Here, docker run creates an container
     -d means detached mode to run in background
     -p means expose port of container 123:321 where 321 is the app port and 321 is binded with docker port

* List Container
docker container ls

* Stop Container
docker stop ContainerName

* Remove container
docker rm ContainerName

* Interact with container
docker exec -it ContainerName bash
    Here, exec means execute the container
    -it means interact with process of the container 


Docker compose is container orchestration system that allows us to deploy, manage, scale and set network to multiple containers using .yaml (yet another markup language) file.

docker-compose up -d --build

* Clean docker unused images, containers and networks
docker system prune -a

* Stop containers
docker-compose down

* Push to docker
docker build -t username/ServiceName:TagName .
docker push username/ServiceName:TagName