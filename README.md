
# Docker-project

Implementing docker within few lines of bash. This project includes pulling image, creating containers, checking container status, running the container, checking logs, executing commands in the container, docker commit and deleting a container/Image.
## Prerequisites
The following packages are needed to run bocker.

    btrfs-progs
    wget
    iproute2
    iptables
    libcgroup-tools
    util-linux >= 2.25.2
    coreutils >= 7.5

## Installation

Installing Docker on your system

Arch

```bash
  sudo pacman -S docker
  sudo systemctl start docker.service
  sudo systemctl status docker.service
  sudo systemctl enable docker.service
  
```
If the above method does not work then first download the package from [Arch](https://docs.docker.com/desktop/release-notes/) release page.
Then do the following 
```bash
  sudo pacman -U ./docker-desktop-<version>-<arch>.pkg.tar.zst
```
Try to install the base version and not the docker desktop for Arch as it is not stable.

Ubuntu

```bash
  sudo apt-get update
  sudo apt install docker.io
  sudo snap install docker  
```
If the above does not work on ubuntu or debian based distros, then try the following
```bash
  sudo apt update
  sudo apt install apt-transport-https ca-certificates curl software-properties-common
  curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
  sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable"
  sudo apt update
  apt-cache policy docker-ce
  sudo apt install docker-ce 
```
## Functionality: Currently Implemented
```
docker build 
docker pull
docker images
docker ps
docker run
docker exec
docker logs
docker commit
docker rm 
```
## Documentation

[Installation](https://docs.docker.com/get-docker/)

[Docker](https://docs.docker.com/get-started/)

[Docker-cheatsheet](https://dockerlabs.collabnix.com/docker/cheatsheet/)


