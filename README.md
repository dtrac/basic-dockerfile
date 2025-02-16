# basic-dockerfile

https://roadmap.sh/projects/basic-dockerfile

In this project, you will write a basic Dockerfile to create a Docker image. When this Docker image is run, it should print “Hello, Captain!” to the console before exiting.

## Requirements
- The Dockerfile should be named Dockerfile.
- The Dockerfile should be in the root directory of the project.
- The base image should be alpine:latest.
- The Dockerfile should contain a single instruction to print “Hello, Captain!” to the console before exiting.

You can learn more about writing a Dockerfile [here](https://docs.docker.com/engine/reference/builder/).

If you are looking to build a more advanced version of this project, you can consider adding the ability to pass your name to the Docker image as an argument, and have the Docker image print “Hello, [your name]!” instead of “Hello, Captain!”.

## Solution

1. Build the container without a custom name argument:
   ```bash
   docker build -t hello-captain .
   ```
2. Run the container:
   ```bash
   docker run --rm hello-captain  
   Hello, Captain!
   ```
3. Build the container with a custom build argument:
   ```bash
   docker build --build-arg NAME=Alice -t hello-captain .
   ```
4. Run the container:
   ```bash
   docker run --rm hello-captain  
   Hello, Alice!
   ```
