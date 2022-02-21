# docker
- Docker 🐳 is an open platform for developers and sysadmins to build, ship, and run distributed applications.
- With Docker, developers can build any app in any language using any toolchain. 
- “Dockerized” apps are completely portable and can run anywhere - colleagues’ OS X and Windows laptops, QA servers running Ubuntu in the cloud, and production data center VMs running Red Hat.
- Developers can get going quickly by starting with one of the 13,000+ apps available on Docker Hub. 
- Docker manages and tracks changes and dependencies, making it easier for sysadmins to understand how the apps that developers build work. 
- With Docker Hub, developers can automate their build pipeline and share artifacts with collaborators through public or private repositories.


#

|  #  | Topics learned                                                                                                              |
| :-: | --------------------------------------------------------------------------------------------------------------------------- | 
| 01  | What is Docker| 
| 02  | Installing Docker| 
| 03  | Images and Containers | 
| 04  | Parent Images & Docker Hub| 
| 05  | The Dockerfile |
| 06  | dockerignore | 
| 07  | Starting & Stopping Containers | 
| 08  | Layer Caching | 
| 09  | Managing Images and Containers | 
| 10  | Volumes | 
| 11  | Docker Compose | 
| 12  | Dockerizing a React App | 
| 13  | Sharing Images on Docker Hub | 

#

## Docker Commands

### Show commands & management commands
```
$ docker
```

### Create a Image
```
$ docker build -t myapp .
```

### Show all Images
```
$ docker images
```

### Run the image and giving the name of container to myapp_c1
```
$ docker run --name myapp_c1 myapp
```

### Show all Containers
```
$ docker ps -a
```

### Stop the container
```
$ docker stop myapp_c1
```

### Specify a port on our computer that can be mapped to exposed the port mapped by the container
```
$ docker run --name myapp_c2 -p 4000:4000 -d myapp
```

### Start an existing container
```
$ docker start myapp_c2
```

### To delete an image
```
$ docker image rm myapp
```

### If it is in use then -f will force remove it
```
$ docker image rm myapp -f
```

### Delete an container
```
$ docker container rm myapp_c2
```

### Remove all Images and Container
```
$ docker system prune -a
```

### Create a new image with a tag version
```
$ docker build -t myapp:v1 .
```

### Running the image and giving the container name
```
$ docker run --name myapp_c -p 4000:4000 myapp:v1
```

### To make the images and running container
```
$ docker-compose up
```

### Stopping the container and removing it
```
$ docker-compose down --rmi all -v
```
