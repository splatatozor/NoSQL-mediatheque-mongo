# NoSQL-mediatheque-mongo

## Outils
 - Docker
 
## Base noSql
 - Mongo
 
## Install Docker

 - sudo apt update
 - sudo apt upgrade
 - sudo apt reboot
 - sudo apt install docker.io
 - sudo dnf install docker
 - curl -fsSL https://get.docker.com/ | sh
 - sudo usermod -a -G docker $USER
 - sudo groupadd docker && sudo gpasswd -a ${USER} docker && sudo systemctl restart docker
 - newgrp docker
 - sudo systemctl start docker
 - sudo systemctl enable docker


## Create Mongo Container

 - docker pull mongo
 - docker run -d -P --name <YourName> -d mongo
 - docker ps -a (Vérification du bon fonctionnement)
 
## Create Mongo Database

 - docker container exec -it <YourName> bash
 - mongoimport --db albums --collection albums --file dumpjson.json --jsonArray
 - mongoimport --db albums --collection artistes --file dump_artistes.json --jsonArray
 - mongo
 - use albums
 - db.albums.find()
