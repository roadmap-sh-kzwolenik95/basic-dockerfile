### Prerequisites:
* docker installed

### How to run:

```sh
docker buildx build -t hello-captain:1.0 .

# List the new image
docker image ls hello-captain

# Run the image
docker run hello-captain:1.0

# List runs:
docker ps -a --filter "ancestor=hello-captain:1.0"


# CLEANUP
# Remove stopped containers:
docker rm $(docker ps -a --filter "ancestor=hello-captain:1.0" -q)

# Remove the image:
docker rmi hello-captain:1.0
```

Project description:

https://roadmap.sh/projects/basic-dockerfile