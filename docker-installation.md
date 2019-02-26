#Docker Installation

##Docker Installation on Linux Operating System

##Centos
For other Operating System Refer
https://docs.docker.com/install/
Uninstall old versions
$ sudo yum remove docker \
                  docker-client \
                  docker-client-latest \
                  docker-common \
                  docker-latest \
                  docker-latest-logrotate \
                  docker-logrotate \
                  docker-engine
Set up the repository
$ sudo yum install -y yum-utils \
  device-mapper-persistent-data \
  lvm2
 
$ sudo yum-config-manager \
    --add-repo \
    https://download.docker.com/linux/centos/docker-ce.repo 
Install Docker CE
$ sudo yum install docker-ce docker-ce-cli containerd.io
Start & Enable Docker.
$ sudo systemctl start docker

$ sudo systemctl enable docker
Uninstall Docker CE
Uninstall the Docker package
$ sudo yum remove docker-ce
Images, containers, volumes, or customized configuration files on your host are not automatically removed. To delete all images, containers, and volumes
$ sudo rm -rf /var/lib/docker
