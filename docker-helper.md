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
docker run -v '/host/directory:/container/directory' image_name | map a directory between host and container
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
docker inspect container_id | show container informations, like mount directory
docker run -p 8080:3000 -v "/home/padovese/Desktop/github/volume-exemplo:/var/www" -w "/var/www" node npm start | start a node application 
docker run --env SPLUNK_START_ARGS="--accept-license --seed-passwd 12345678" -it --name splunk -p 8000:8000 -p 9997:9997 splunk/splunk | start a splunk app
docker images | show all local images
docker build -f node.dockerfile -t padovese/node . | build a dockerfile
docker run -d -p 8080:3000 padovese/node | start the container
docker login | log into dockerhub
docker push image_name | push an image
docker pull image_name | pull an image
docker network create --driver bridge my-network | create a docker network
docker network ls | list all docker's networks
docker run -it --name my-contrainer --network my-network ubuntu | create a container inside my network
docker exec -ti my-container bash | enter in a container that is running(in bash case), or exec any application
docker cp script.sh container_name:absolute_path | cp, like a regular cp or scp
