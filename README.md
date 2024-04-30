# Getting started

This repository is a sample application for users following the getting started guide at https://docs.docker.com/get-started/.

The application is based on the application from the getting started tutorial at https://github.com/docker/getting-started


How to run: 

- I have added `Dockerfile` already to this project: getting-started-docker. Ideally, you can create one from docs.docker.com/get-started

- Once Dockerfile is ready, build your container image using (you must have docker installed on your machine).
    - Dockerfile needs to be in the root dir of the project. 
    - You need to run the following command from the root directory of the project, In this case: getting-started-docker
    - `docker build -t getting-started-docker .`


- Start the app from your container: 
    `docker run -dp 127.0.0.1:3000:3000 getting-started-docker`
    - -d flag (short for --detach
    - -p flag (short for --publish) creates a port mapping between the host and the container.
        in the Dockerfile: expose 3000 will map the container port 3000 to the host port at 3000 (in this case, localhost).
- Check running containers: 
    - `docker ps`
    - stop a running container:
        `docker stop {container_id}`
    