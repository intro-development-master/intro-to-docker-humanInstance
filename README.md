# Intro to Docker

The purpose of this lesson is to teach the fundamentals of [Docker](https://www.docker.com/what-docker). Docker's documentation can be found [here](https://docs.docker.com/).

## What is Docker

Docker is a platform for developers and sysadmins to **develop, deploy, and run** applications with containers.

What is Containerization?

The act of using containers to deploy applications is called containerization.

Containers allow:

* Flexibility: Complex apps can be containerized
* Lightweight: Containers leverage and share the host kernel
* Interchangeable: Can deploy updates and upgrades on-the-fly
* Portable: Build locally, Deploy to the cloud, Run anywhere
* Scalable: Increase and automatically distribute container replicas
* Stackable: Stack services vertically and on-the-fly

### Images and Containers

A container is launched by running an image.  An image is an executable package that includes everything that is needed to run an application, code, runtime libraries, environment variables, and configuration files.

### Containers vs Virtual Machines (VMs)

A **container** runs _natively_ on Linux and shares the kernel of the host machine with other containers. It runs a discrete process, taking no more memory than any other executable, making it lightweight.

By contrast, a **virtual machine** (VM) runs a full-blown “guest” operating system with _virtual_ access to host resources through a hypervisor. In general, VMs provide an environment with more resources than most applications need.

## How to Use Docker

Docker uses various commands to interact with containers.

Once installed, you can start using Docker!

### Lifecycle Commands

`docker --version` - Displays current Docker version

`docker run` - Creates and starts a container

`docker rm` - Removes a container

To run a container, use the commmand `docker run -d <container id>`.  The `-d` flag will detach the container automatically, so it runs in the background.

If you want to run a transient container, use the command `docker run --rm`.

### Starting and Stopping

`docker start` - Starts a container (running)

`docker stop` - Stops a running container

`docker restart` - Restarts a container

### Info Commands

`docker ps` - Shows running containers

`docker ps -a` - Shows all containers

### Executing Commands

`docker exec` - To execute a command in a container

To enter a running container, use the command `docker exec -it <container id> /bin/bash`.

### Image Commands

`docker images` - Shows all images.

`docker build` - Creates image from Dockerfile.

`docker rmi` - Removes an image.

## Images

Images can be manually built, or they can be comprised on multiple other images. To search from various images, visit [DockerHub](https://hub.docker.com/).