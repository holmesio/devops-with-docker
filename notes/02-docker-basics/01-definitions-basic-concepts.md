# Definitions and Basic Concepts


*DevOps*, made up of *Dev* (development of software) and *Ops* (operations), is the release, configuration, and monitoring of software that is in the hands of the very people who develop it.

*Docker* is a set of platform as a service (PaaS) products that use OS-level virtualization to deliver software in packages called containers.

*Containers* differ from standard virtual machines, offering faster startup, better resource utilization, and high portability across different environments. Unlike virtual machines, their isolation is at the process level, which may not be as robust as that of VMs.

*Images* are files that containers use to run applications. If containers are meals, then images are the recipe and ingredients needed to create the meal.

Images never change, therefore existing files cannot be edited. To create a new one, you start from a base image and add new *layers* to it. 

Image files are built from instructional files called *Dockerfiles*, which look something like this:

```dockerfile
FROM <image>:<tag>

RUN <install some dependencies>

CMD <command that is executed on `docker container run`>
```

Returning to the meal analogy, if images are ingredients and the recipe for containers, then Dockerfiles are recipes for the images. We write the Dockerfile, and the image is written by our machine based on that Dockerfile.

## Docker CLI Commands

- `docker run -d <image>`: Starts a container *detached*, meaning it runs in the background. 
- `docker image ls`: Lists all images.
- `docker image rm <image>`: Removes an image.
- `docker image pull <image>`: Pulls image from a docker registry.
- `docker container ls -a`: Lists all containers.
- `docker container run <image>`: Instructs the Docker daemon to create a container from the image and downloading the image if it's not available.
- `docker container rm <container>`: Removes a container.
- `docker container stop <container>`: Stops a container.
- `docker container exec <container>`: Executes a command inside the container.
