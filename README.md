Docker Demo
===========

### Docker machine setup

* run `docker-machine create -d virtualbox --virtualbox-memory 4096 --virtualbox-cpu-count 2 --virtualbox-disk-size 40000 --engine-storage-driver overlay default`
* run `docker-machine start default`
* run `eval "$(docker-machine env default)"`
* run `docker-machine env default | grep DOCKER_HOST`
* Write down the ip that is printed by the last command

### Simple apache2 dockefile

* go to ./docker-demo
* run `docker build -t docker-demo .`
* run `docker run -it --rm --net host docker-demo`
* open a browser and and use the ip with the default port (80) from the previous instructions
* after the test press `CTRL-C` to kill the apache server

### Wordpress on docker-compose

* go to ./docker-compose
* run `docker-compose up -d`
* open a browser and and use the ip and port 8080 from the previous instructions


