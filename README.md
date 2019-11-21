Dockerfile
==========
1. Manifest file. Static text.
2. Contains all dependencies for the app including the artifact
3. Use existing base images (mostly linux based)
4. Alpine vs Other linux (Ubuntu vs Centos)


Commands:
=========
docker pull [image]
docker run -d -p 3000:80 [image]

docker container ls
docker ps

docker image ls
docker images

docker build -t [image_name] .
docker push [image_name]
docker tag [image_name] [name:tag]


docker rm [containerid]
docker rmi [imageid]




Docker Compose
==============
1. Run containers together with internal networking
3. Can be used easily for integration tests or local setup of clusters
4. No ability to self-heal, load balancing, scaling



Commands:
=========
docker-compose up -d
docker-compose down


Docker Volume
=============
1. Containers are ephemeral. Data is lost once they exit.
2. Volume is a way to mount a host directory within the container.

    volumes:
      - type: bind
        source: ./database-dir
        target: /var/lib/postgresql/data

Commands:
=========
docker volume ls


Cleaning Up
===========
docker container prune -af
docker image prune -f
docker volume prune -f

