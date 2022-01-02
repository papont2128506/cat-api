#Cat-api

###start db service:
    docker-compose -f compose-env.yaml up -d

###build docker image
chmod +x build_and_push.sh

###start docker container
~~docker run -ti --rm trusoff/cats-api:1.0.0~~

docker run -ti --rm -e DATASOURCE-HOST=192.168.0.130 trusoff/cats-api:1.0.0

###drop docker container
docker rmi trusoff/cats-api:1.0.0

###push image
docker push trusoff/cats-api:1.0.0

###pull image
docker push trusoff/cats-api:1.0.0