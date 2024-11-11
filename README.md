# Docker helper

## Run

https://docs.docker.com/engine/reference/run/

    docker run hello-world 
    # -p 8080:80 ( --publish )
    # -d (demonize)
    # -it (interactive)


**Launch a shell on a running container**
    
    docker exec -it ${name} bash


Commands: ps, stop, rm, top, logs


## Network

    docker network ls
    docker network inspect ${name}
    docker network create ${name}


I can specify a network when starting a container `--network ${name}`

I can interconnect a docker and a network (disconnect is also available) `docker network connect ${network_name} ${container_name}`


## Data persistence

https://docs.docker.com/storage/


### Volumes
docker volume ls
docker volume inspect ${name}
docker volume prune


-v : ?
Bind mount

## Docker compose

https://docs.docker.com/compose/compose-file/ 

Déconseillé pour la prod.

Commands: up, down, ps, top

### Image
docker image history ${name}
docker image inspect ${name}
docker image ls


## Other

    docker version
    docker info
    docker login
    docker exec -it <container> bash
