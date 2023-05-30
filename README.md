## create mysql container
docker run --name mysql-8-container -e MYSQL_ROOT_PASSWORD=codelink@123 -p 3306:3306 -d mysql:latest

## for chaking preosess
docker ps

# mysql -h 127.0.0.1 -P 3306 -u sail -p password

## push the code on docker 
# add tag of image 
docker tag laravel_sail_image mydockerhubuser/laravel_sail:1.0.0

# login docker 
docker login

# push the code 
docker push mydockerhubuser/laravel_sail:1.0.0

# pull the code 
docker pull mydockerhubuser/laravel_sail:1.0.0

# docker exec -it <container_name> <command>
```
docker run: Create and start a new container based on an image.
docker ps: List running containers.
docker images: List available images.
docker pull: Download an image from a registry.
docker build: Build a new image from a Dockerfile.
docker stop: Stop a running container.
docker rm: Remove a container.
docker rmi: Remove an image.
docker exec: Run a command in a running container.
docker logs: Fetch the logs of a container.
docker inspect: Retrieve detailed information about a container or image.
docker network: Manage Docker networks.
docker volume: Manage Docker volumes.
docker cp: Copy files/folders between a container and the host.
docker-compose up: Create and start containers defined in a Compose file.
docker-compose down: Stop and remove containers defined in a Compose file.
docker-compose build: Build or rebuild services defined in a Compose file.
docker-compose logs: Fetch the logs of services defined in a Compose file.
docker-compose exec: Run a command in a service container.
docker-compose pull: Pull images for services defined in a Compose file.
```
# delate image,container, volumns
docker image prune <name> -f

## sail commands
```
  sail up        Start the application
  sail up -d     Start the application in the background
  sail stop      Stop the application
  sail restart   Restart the application
  sail ps        Display the status of all containers
  sail artisan queue:work
  sail mysql     Start a MySQL CLI session within the 'mysql' container
  sail php -v
  sail share     share the application
```
https://tech.osteel.me/posts/you-dont-need-laravel-sail
