# ***Basic-Docker-Commands***

```

sudo curl -sSL https://get.docker.com/ | sh
docker --version
dpkg -l|grep docker
docker run ubuntu
docker images
docker ps
docker ps -a
docker inspect feaa
docker images history
docker images
docker history 216
docker ps -a
docker start feaa
docker attach feaa
docker run -d ubuntu
docker run ubuntu sleep 10
service docker status
docker exec c02db cat /etc/hosts
docker search ubuntu
docker run redis
docker rm c02 9a2 feaa
docker rm 9ae
docker run redis:4.0
docker images
docker rmi 191
echo test | docker run -i busybox cat
docker inspect 2503
docker inspect -f "{{.State.StartedAt}}" 250
echo $?
docker run -it --name mycontainer1 ubuntu /bin/bash
docker diff -h
docker diff --help
docker diff mycontainer1
docker commit mycontainer1 myimage1
docker run -it --name mycontainer2 myimage1 /bin/bash
docker build -t second -f /home/prasoon_prit/docker-file/dockerfile-new/Dockerfile .
docker images prune
docker rmi -f$(docker images -q)
docker images
docker stop $(docker ps -a -q)
docker rm $(docker ps -a -q)
docker rmi -f $(docker images -q)
docker rmi a78 216 ff4
docker images
docker run -it --name cont2 --privileged=true --volumes-from cont1 ubuntu /bin/bash
docker attach cont1
docker exec -it cont2 /bin/bash
docker start cont2
docker run -it --name cont3 --volumes-from cont2 ubuntu /bin/bash
docker run -it --name cont4 -v /volume2 ubuntu /bin/bash
docker run -it --name cont5 --privileged=true --volumes-from=cont4 ubuntu /bin/bash
docker run -it --name hostcontainer -v /home/prasoon_prit:/container ubuntu /bin/bash
docker volume create myvolume
docker volume ls
docker volume inspect 3d1
docker volume inspect 3d14cfd3ebdaf3772c69c69443c0e1a0ccc47d5145682fe62264ced92203c2bf
docker volume inspect myvolume
docker volume rm 3d14cfd3ebdaf3772c69c69443c0e1a0ccc47d5145682fe62264ced92203c2bf
echo "creating bind volume mount" >> /home/prasoon_prit/bindvolume/xyz.txt
docker run -it --mount type=bind,source=/home/prasoon_prit/bindvolume,target=/container \ubuntu /bin/bash
docker volume prune
docker run -d --name portexpose -p 80:80 ubuntu
docker run -td --name portexpose -p 80:80 ubuntu
docker run -td --name portexpose -p 80:80 ubuntu
docker search jenkins
docker run -td --name jenkins -p 8080:8080 jenkins/jenkins
docker ps 
docker port jenkins
docker rm $(docker ps -a -q)
docker stop $(docker ps -a -q)
docker rm $(docker ps -a -q)
docker inspect ubuntu
docker inspect ubuntu | grep net*
docker run ubuntu --network=none
docker container ls -l
docker run --network=none ubuntu
docker run --network=host ubuntu
docker inspect 835d | grep -i network*
root@docker-learning:/home/prasoon_prit# docker system
Usage:  docker system COMMAND
Manage Docker
Commands:
  df          Show docker disk usage
  events      Get real time events from the server
  info        Display system-wide information
  prune       Remove unused data

docker-compose up
docker-compose up -d
docker-compose down
docker-compose config
docker-compose images
docker-compose ps
docker-compose top
docker container ls -a
docker container pause 832
docker container unpause 832
docker container prune
docker system
docker system df
docker system info
docker system prune -a
docker top 9009722eac4d
docker stats 9009722eac4d
docker system events
docker container run -p 5000:5000 -d -m 512m --cpu-quota=50000  prasoon/hello-world-java:0.1
docker container stats 4faca1ea914e3e4587d1d790948ec6cb8fa34f26e900c12632fd64d4722fd59a
docker stats 42f170966ce613d2a16d7404495af7b3295e01aeb9142e1fa1762bbdc581f502
docker network ls
docker network inspect bridge
docker run --cpus=.5 ubuntu
docker run --memory=100m ubuntu

```

