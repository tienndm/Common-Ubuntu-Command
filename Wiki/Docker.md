# Ubuntu Docker command
Docker provides various commands to manage containers, images, networks, and volumes. Below are some of the most common Docker commands along with explanations of their arguments.

## 1. Docker pull
Pull a Docker image from Docker Hub or another registry.

```bash
docker pull <image_name>:<tag>
```

## 2. Docker build
Build an image from a Dockerfile.
```bash
docker build -t <image_name>:<tag> <path_to_dockerfile>
```

## 3. Docker run
Create and run a container from an image.
```bash
docker run -d --name <container_name> -p 80:80 <image_name>
```
- `-d`: Run the container in detached (background) mode.
- `-p <host_port>:<container_port>`: Map ports between the host and the container.
- `--name <container_name>`: Name the container.
- `<image_name>`: The name of the image to use for creating the container

# 4. Docker ps
List the running containers.
```bash
docker ps
```
- `-a`: Show all container, including those that are stopped.
- `-q`: Show only container IDs.

# 5. Docker stop
Stop a running container.
```bash
docker stop <container_id_or_name>
```

# 6. Docker start
Start a stopped container.
```bash
docker start <container_id_or_name>
```

# 7. Docker restart
Restart a container (stop and start it again)
```bash
docker restart <container_id_or_name>
```

# 8. Docker rm
Remove a container.
```bash
docker rm <container_id_or_name>
```
-`-f`: Force remove the container even if it's running.
-`-v`: Remove volumes associated with the container.

# 9. Docker rmi
Remove an image from the local machine.
```bash
docker rmi <image_id_or_name>
```
-`-f`: Force remove the image even if it's being used by a container.

# 10. Docker logs
View the logs of a container.
```bash
docker logs <container_id_or_name>
```
-`-f`: Follow the log output in real time.
-`--tail <number>`: Show a  specific number of recent log lines.

# 11. Docker exec
Run a command inside a running container.
```bash
docker exec -it <container_id_or_name> <command>
```
-`-i`: Keep STDIN open (useful for interactive commands).
-`-t`: Allocate a TTY (terminal) for command interaction.
-`<command>`: The command to run inside the container, e.g., bash to access the container's shell.

# 12. Docker images
List all images on the local machine.
```bash
docker images
```
-`-q`: Show only image IDs.

# 13. Docker network ls
List all Docker networks.
```bash
docker network ls
```

# 14. Docker volume ls
List all Docker volumes.
```bash
docker volume ls
```

# 15. Docker-compose up
Start services defined in a `docker-compose.yml` file.
```bash
docker-compose up
```
-`-d`: Run the containers in detached (background) mode.
-`--build`: Force rebuild the image before starting the container.

# 16. Docker-compose down
Stop and remove all containers, networks, volumes, and images created by `docker-compose up`.
```bash
docker-compose down
```
-`-v`: Remove volumes associated with the containers.

# 17. Dockerhub login
Log in to Dockerhub account.
```bash
docker login -u <username>
```

# 18. Dockerhub tag image
Tagging the image with Dockerhub username and repository name.
```bash
docker tag <image_name>:<tag> <username>/<repository_name>:<tag>
```

# 19. Dockerhub push image
Pushing image to Docker Hub
```bash
docker push <username>/<repository_name>:<tag>
```
