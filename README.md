# P21CS013
CSL7510 Assessment 1: Virtual Machines & Dockers

Installing Docker on Ubuntu 20.04 VM on Virtual Box; best for native experience 

Getting docker latest version from  get.docker.com script (latest Edge release) 

	curl -fsSL https://get.docker.com -o get-docker.sh
  
	sh get-docker.sh
  
sudo usermod -aG docker bret -adding my user account to docker group on the system (to avoid sudo every time)

sudo docker version  Docker Engine - Community Version: 20.10.8

sudo docker run hello-world

After installing Docker, get docker-compose and dockermachine from 

https://docs.docker.com/machine/install-machine

base=https://github.com/docker/machine/releases/download/v0.16.0 \ && curl -L $base/docker-machine-$(uname -s)-$(uname -m) >/tmp/docker-machine \ && mv /tmp/docker-machine /usr/local/bin/docker-machine \ && chmod +x /usr/local/bin/docker-machine 

https://docs.docker.com/compose/install

curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose 

Install git- sudo apt install git

command: docker version –check if verified cli can talk to engine 
command: docker info –check  most config values of engine

Container VS Virtual Machine: Containers are just processes. Limited to what resources they can access (file paths, network devices, running processes). Exit when process stops

Image vs. Container:   An Image is the application we want to run. A Container is an instance of that image running as a process We can have many containers running off the same image. Docker's default image "registry" is called Docker Hub (hub.docker.com) 

I have have cloned the dockerfile from my github 
santosh@santosh-VB:~/demo-2048/code/P21CS013/dockerfile$ ll
total 16
drwxrwxr-x 2 santosh santosh 4096 Sep  1 09:09 ./
drwxrwxr-x 4 santosh santosh 4096 Sep  1 09:09 ../
-rw-rw-r-- 1 santosh santosh  348 Sep  1 09:09 Dockerfile
-rw-rw-r-- 1 santosh santosh  271 Sep  1 09:09 index.html

git clone https://github.com/Santosh-P21CS013/P21CS013.git
git pull

BUILDING THE IMAGE-
sudo docker image build -t ngixn-with-html .

RUNNING THE CONTAINER-
sudo docker container run -p 80:80 --rm ngixn-with-html
