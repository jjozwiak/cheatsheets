## Definitions

* **image** - An immutable (unchangeable) file that contains the source code, libraries, dependencies, tools, and other files needed for an application to run. An image is a template for a container.
* **container** - A virtualized run-time environment where users can isolate applications from the underlying system. These containers are compact, portable units in which you can start up an application quickly and easily.

## Commands

| Command | Example |
|---|---|
| ```docker run ``` | |

## Flags

| Flag | Desc |
|---|---|
| -it | interactive |
| --rm | removes container after exiting |

## Dockerfile

| Instructions  |   | |
|---|---|---|
| FROM | FROM <image> | defines base image to use |
| WORKDIR | WORKDIR /path/to/directory | sets current working directory for RUN, CMD, ENTRYPOINT, COPY, and ADD instructions |
| ADD | | |
| COPY | | |
| RUN  |   | |
| CMD  |   | |
| ENTRYPOINT | |   |
| ENV | | |
| VOLUME | | |
| LABEL | | |
| EXPOSE | | |
