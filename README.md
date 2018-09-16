# Docker quickstart
A simple docker to quickly start with PHP, MySQL and Xdebug
## Setup
```php
$ git clone https://github.com/DeSuper/docker-quickstart.git project  
$ cd project
$ rm -rf .git
$ cp .docker/.env.example .docker/.env
$ docker-compose up
```
Go to: http://localhost:8080/
## Issues
I ran into some issues running Docker on my Windows 10. These link might help:
### Firewall
Docker said my firewall was in the way and pointed to some documentation to open up a port.
I never found this option in my firewall, but ran into a Powershell command that makes windows trust the network with Docker
```php
Set-NetConnectionProfile -interfacealias "vEthernet (DockerNAT)" -NetworkCategory Private
```
Source: https://stackoverflow.com/questions/42203488/settings-to-windows-firewall-to-allow-docker-for-windows-to-share-drive
### Authorisation
Log into Docker with your username, not your e-mailaddress.

Source:https://forums.docker.com/t/unauthorized-incorrect-username-or-password/35677/2
## Usefull commands
```php
$ docker exec -it <<container name>> /bin/bash
$ docker-compose -d up
$ docker-compose stop
$ docker compose halt
```
## Bitbucker Pipelines
### Using docker-compose in pipelines
* https://medium.com/magnetcoop/using-docker-compose-in-bitbucket-pipelines-81ead8cf0153  
* https://bitbucket.org/magnet-coop/bitbucket-pipelines-docker-compose/src/master/  
* https://hub.docker.com/_/docker/
 