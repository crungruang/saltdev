# Saltstack Docker Dev

### Prerequisites
* Set a REPO_HOME environment variable to the directory ABOVE this saltdev.git project on your host machine

## Getting Started
From the saltdev folder run:
```
docker-compose up -d --build
```
Check that keys were accepted and minions are responding:
```
docker exec salt-master salt '*' test.ping
```
### To Destroy
```
docker-compose stop && docker-compose rm -f
```
## Purpose
I wanted to provide a generic, reusable set of examples that can be used to play with Docker and Salt. 

### Features
* change out O/S via Dockerfile
* destroy and recreate containers using docker-compose
* salt and pillar folders in this project are mounted on salt master
