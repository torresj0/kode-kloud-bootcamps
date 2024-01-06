# DOCKER ON KODEKLOUD

### Exercises

Run an instance of kodekloud/simple-webapp
with a tag blue and map port 8080 on the
container to 38282 on the host.

**SOLUTION** -> ``` docker run -p 38282:8080 kodekloud/simple-webapp:blue ```

___

### Docker Images
```docker images``` shows the running images

___
We just downloaded the code of an application.
What is the base image used in the Dockerfile?

Inspect the Dockerfile in the webapp-color directory.

```cat /root/webapp-color/Dockerfile```

___
Build a docker image using the Dockerfile and name
it webapp-color. No tag to be specified.
```docker build -t webapp-color```

___
Run an instance of the image webapp-color and publish
port 8080 on the container to 8282 on the host.
```docker run -p 8282:8080 webapp-color```

___
Build a new smaller docker image by modifying the same
Dockerfile and name it webapp-color and tag it lite.
Hint: Find a smaller base image for python:3.6.
Make sure the final image is less than 150MB.

In the webapp-color directory, run the ls -l command to list the Dockerfile and other files.

And modify Dockerfile to use python:3.6-alpine image and then build using
```docker build -t webapp-color:lite .```

### The use of ```i``` and ```t``` in Docker

`docker run kodekloud/simple-prompt-docker`
output `
Hello and welcome
`
Adding de -i parameter to the command allows you to enter your name
in an iterative way
`docker run -i kodekloud/simple-prompt-docker`
output 
`
Hello and welcome Joao
`
___
## Docker compose
First create a redus database container called `redis`, image `redis:alpine`.
run command `docker run --name -d redis:alpine`
