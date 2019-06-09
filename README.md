# README

## COMANDOS DOCKER
* Informações do docker: `docker info`
* Instâncias em execução: `docker ps`
* Parar uma instância: `docker container stop ID` ou `docker container stop name`
* Iniciar uma instância: `docker container start ID` ou `docker container start name`
* Download de uma imagem: `docker pull sapk/cloud9`
* Executando Cloud9: `docker run -d -p 8181:8181 sapk/cloud9 --auth username:password`
* Listando imagens: `docker images`
* Removendo uma imagem: `docker rmi ID` ou `docker rmi name`
* Listando containers: `docker container ls`
* `docker container prune`


## IMAGE UBUNTU
* `docker pull ubuntu`
* `docker run -i -t ubuntu /bin/bash`
* Terminal interativo: `docker container exec -it ID top`
* Background -> foreground: `docker container attach ID`

## IMAGE NGINX
* `docker pull nginx`
* `docker container run --publish 8080:80 nginx` ou `docker container run -p 8080:80 nginx`
* Detach/Background: `docker container run -p 8080:80 -d nginx`

