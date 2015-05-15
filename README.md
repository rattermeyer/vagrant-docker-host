# Docker development box
This box defines a docker development environment. It basically installs

* [docker](https://www.docker.com/whatisdocker/)
* [docker-compose](https://docs.docker.com/compose/)
* [Consul](https://github.com/progrium/docker-consul)
* [Registrator](https://github.com/gliderlabs/registrator)
* [Shipyard](http://shipyard-project.com/)
* git
* vim + useful vim plugins

## Get up and running

* Have enough memory (VM requires 2GB) available. Change settings, if required, in Vagrantfile
* Install [Vagrant](http://vagrantup.com)
* Clone this repository `git clone https://github.com/rattermeyer/vagrant-docker-host`
* Provision a box `vagrant up`
    You need to reboot after the provisioning: `vagrant halt && vagrant up`
* Login `vagrant ssh` or using putty / ssh on localhost:2222

