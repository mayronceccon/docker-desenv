docker-compose up --build
docker-compose up

docker ps
docker exec -it <containerIdOrName> bash

docker stop $(docker ps -a -q)
docker rm $(docker ps -a -q)