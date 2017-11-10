# Docker

Docker is what we use to bundle up all application dependencies (ie. node version, node modules, pdf generator, etc) A docker 'container' is like a mini computer (with full OS, etc) running one specific application.

## Terms

**Docker container:** A instance of an image

**Docker image:** A compiled set of instructions describing the application package

## Tutorial
1. Grab Docker for mac from [here](https://docs.docker.com/docker-for-mac/install/) and install it.

2. Try running nginx (a simple web server)

	`docker run -d -p 80:80 --name webserver nginx`

	This downloads the nginx image and runs a container named _webserver_ on port 80, linking it to port 80 on the local machine.

	Now hit [http://localhost](http://localhost) in your browser and you should see the nginx welcome screen


3. Show running containers

	`docker ps`

	Should list running containers, while `docker ps -a` lists all containers running and stopped.

4. Stop and start containers

	Run `docker stop webserver` to stop the webserver.
	
	Run  `docker start webserver` to start it again.

5. Cleaning up

	Run `docker rm -f webserver` to delete the webserver container.

	Run `docker rmi nginx` to remove the nginx image.
