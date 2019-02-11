# Creating and Using Containers

## Check docker --help for command usages

docker version

""" Shows the version of both docker client and docker host """


docker info

"""  To show more details about your docker environment . For ex , how many containers are running , is swarm mode active or not? ... and so on """


docker

""" Executing docker without any arguments will show you the help page """


docker container run <image-name>

docker run

# Our First Container 
## Starting a Nginx Web Server

docker container run --publish 80:80 nginx

""" --publish or -p are used to forward traffic from host to container . The format is "<host-port>:<container-port>" """


docker container run --publish 80:80 --detach nginx

docker container ls

docker container stop <container-id>

docker container ls

docker container ls -a

docker container run --publish 80:80 --detach --name webhost nginx

""" --detach or -d is used to start the container in background . You can attach the terminal back when needed """


docker container ls -a

docker container logs webhost

""" To see logs of a container """


docker container top

docker container top webhost

""" Shows the top processes in your containers """


docker container --help

docker container ls -a

docker container rm <container-id> <container-id> <container-id>

""" To remove containers. multiple container id can be passed as arguments """


docker container ls
