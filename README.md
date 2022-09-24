# DevSecOps_Tutorial
Repo for demonstration how to implement the Github free Security features. 


# Table of contents:

- [Quickstart](#quickstart)
- [Pre-reqs](#pre-reqs)
- [Getting started](#getting-started)
- [Docker commands](#docker-commands)
- [Notes](#notes)

# Contributors
cyberconchas

# Quickstart
- To build the docker image
```
npm run build
```
- To start the docker container
```
npm run start
```
The application is now serving and available at `localhost:80` and `127.0.0.1:80`

# Pre-reqs
To build and run this app locally you will need a few things:
- Install [Node.js](https://nodejs.org/en/)
- Install [Docker](https://www.docker.com/products/docker-desktop/)
- Install [VS Code](https://code.visualstudio.com/)

# Getting started

- Clone the repository
```
git clone https://github.com/Cyber-JiuJiteria/DevSecOps_Tutorial.git
```
- Navigate to root of the repository
```
cd DevSecOps_Tutorial/
```
- To build the docker image
```
npm run build
```
- To start the docker container
```
npm run start
```
- The container is now started and serving HTML content to the specified port. 
- In the `Package.json start` script, we can see we specified port 80 with `--p 80:80`
- Thus, the Web Page will be serving content on `localhost:80` and `127.0.0.1:80` in any browser 

# Docker commands
- List containers to get container id
```
docker container ls
```
- Stop a container
```
docker stop <CONTAINER_ID>
```
- Delete a container
```
docker rm <CONTAINER_ID>
```

# Notes
- Before starting a new container, be sure to create a new image and stop the current container. Only one container can run on a single port.
- The HTML that we see is being served via an NGINX web server. NGINX serves to port 80 by default
-To alter the port we serve HTML to, simply alter the left number in the `-p 80:80` command
- For example, to serve to `localhost:3000` alter the `run` script to `docker run -d -p 3000:80 devsecops_tutorial`

