<h1>Useful docker commands</h1>

Command  | Description
------------- | -------------
docker version  | see if it's installed and it's version
docker run image_name | download or use a local image to start a container
docker run -d image_name | download or use a local image w/o lock the terminal
docker run -d -P image_name | download or use a local image and set a random port
docker run -d -p 12345:80 image_name | download or use a local image and set a fixed port
docker run -it image_name | download or use a local image and get in the container
docker run --name personal_name image_name | set a name to the container
docker run -d -P -e AUTHOR="PADOVESE" dockersamples/static-site | pass a parameter to docker application
docker ps  | show running containers
docker ps -a | show all containers
docker start container_id | start a container
docker start -a -i container_id | start and enter in the container
docker stop container_id | stop a container in 10s
docker stop -t 0 container_id | stop a container immediately
docker stop -t 0 $(docker ps -q) | stop all containers
docker rm container_id | remove a container
docker container prune | remove all containers
docker rmi image_name | remove a local image
docker port container_id | list container's port