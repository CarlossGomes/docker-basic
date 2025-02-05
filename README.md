# Learning docker

Some Important commands

    -Command to list images
    docker images

    -Command to check the process status
    docker ps

    -Command to generate a build
    docker build -t app-node:1.0 .

    -Comand to run an image
    docker run -d -p 8080:3000 app-node:1.0

    -Command to stop all the images by getting the images id
    docker stop $(docker container ls -q)

    -Command to remove all containers
    docker container rm $(docker container ls -aq)

    -Command to remove all images
    docker rmi $(docker image ls -aq)

    -Command to push image to dockerhub
    docker push image-name/app-node:1.0

    -Command to create a tag from an existing image
    docker tag image-name-old/app-node:1.2 image-name-new/app-node:1.2

    -Command to mount a volume
    docker run -it --mount type=bind,source=C:/volume-docker,target=/app
    docker run -it -v volume-docker:app

    -Command to mount temporary a volume
    docker run -it --mount type=tmpfs,destination=/app
    docker run -it --tmpfs=/app ubuntu bash


    -Command to create a volume
    docker volume create docker-volume

    -Command to create network
    docker network create -d bridge my-bridge-network


    -Types of network
    bridge: allow the containers to communicate with each other and with the oustide world
    host: mode that docker container shares its network namespace with the host machine
    none: none isolates the container by setting the network to null

    -Docker compose commands
    docker-compose up: command to execute docker-compose.yml file
