## Definitions

* **image** - An immutable (unchangeable) file that contains the source code, libraries, dependencies, tools, and other files needed for an application to run. An image is a template for a container.
* **container** - A virtualized run-time environment where users can isolate applications from the underlying system. These containers are compact, portable units in which you can start up an application quickly and easily.

## Commands

| Command |  |
|---|---|
| ``` docker run ``` | |
| ``` docker rm ```| |
| ``` docker rmi ``` | |
| ``` docker images ``` | list images |
| ``` docker ps ``` | list running containers |
| ``` docker ps -a ``` | list all containers even those not running |
| ``` docker build ``` ||
| ``` docker start ``` ||
| ``` docker stop ``` ||


## Flags

| Flag | Example | Description |
|---|---|---|
| -it | | interactive |
| --rm | | removes container after exiting |
| -p | 5000:80 | port publishing where mapping format is \<host\>:\<container\> |
| -v | $(pwd):/var/www/html | set up a volume \<host\>:\<container\> |

## Dockerfile

| Instructions  | Example  | Description |
|---|---|---|
| FROM | FROM \<image\> | Defines base image to use |
| WORKDIR | WORKDIR /path/to/directory | Sets current working directory for RUN, CMD, ENTRYPOINT, COPY, and ADD instructions |
| ADD | ADD index.html /var/www/html | Transfer files from host to container. Supports tarball auto extraction and remote URLs. |
| COPY | COPY index.html /var/www/html | Transfer files from host to container. |
| RUN  | RUN apt-get update (shell form), RUN ["executable", "param1", "param2"] (exec form)  | Executes any command in a new layer on top of current image **during build time**. |
| CMD  | CMD curl, CMD ["executable", "param1", "param2"]  | Executes command when container is **running** |
| ENTRYPOINT | |   |
| ENV | ENV LOGS_DIR="/var/log" | Sets environment variables of a container. |
| VOLUME | VOLUME /var/logs/nginx | Creates a directory on the host and mounts it on the container. |
| LABEL | LABEL key=value | Add metadata to an image with by key value pair. |
| EXPOSE | EXPOSE 80, EXPOSE 53/tcp | Tells Docker the container listens for the specified network ports at runtime. EXPOSE does not publish the port, for this you need to use the -p flag |
