# Docker Cheatsheet
A list of commonly-used docker commands

# Running containers
Run a container:
```
docker run <flags> <image_name> <launch_command>
```
ie. `docker run -ti node /bin/bash`

Stop a container:
```
docker rm -f <container_name>
```

# Working with images
List images:
```
docker images
```

View the layers contained in an image:
```
docker history <image_name>
```

Pull an existing image from the repository:
```
docker pull <image_name>
```

To remove an image:
```
docker rmi <image_name>
```

Commit a change to an image:
```
docker commit -m "<commit_message>" -a "<commit_author>" <container_id> <new_image_name>
```

Build an image from a Dockerfile:
```
docker build --tag <image_name> <folder_containing_dockerfile>
```
ie. `docker build marcpeters/test_image:v2 .`
