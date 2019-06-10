# README

## COMANDOS DOCKER
* Informações do docker: `docker info`
* Instâncias em execução: `docker ps`
* Parar uma instância: `docker container stop ID` ou `docker container stop name`
* Iniciar uma instância: `docker container start ID` ou `docker container start name`
* Listando imagens: `docker images`
* Removendo uma imagem: `docker rmi ID` ou `docker rmi name`
* Listando containers: `docker container ls`
* `docker container prune`
* Inspecionar uma imagem: `docker image inspect ID`
* Inspecionar um container: `docker container inspect ID`
* Renomear container: `docker rename my_container my_new_container`
* Docker commit(gerar novo container a partir de container já criado):
`docker container commit -m 'message' ID`
* `docker image history ID`
Uma imagem é formada por camadas. Um novo commit gera uma camada a mais.
* Opção -P: porta dinâmica
* `docker port ID` -> 22/tcp -> 0.0.0.0:32768
* `docker network ls`

### VOLUMES
Uma imagem pode disponibilizar volumes. Quando o container é montado, por consequência, o volume também será montado.
Resumidamente: volumes são mecanismos preferidos para persistir dados gerados/usados pelo docker.
* Listar volumes: `docker volume ls`
* Inspecionar: `docker volume inspect ID`

## IMAGE CLOUD9
* Download de uma imagem: `docker pull sapk/cloud9`
* Executando Cloud9: `docker run -d -p 8181:8181 sapk/cloud9 --auth username:password`
* `docker run -d -p 8181:8181 -p 3000:3000 sapk/cloud9 --auth username:password`

## IMAGE UBUNTU
* `docker pull ubuntu`
* `docker run -i -t ubuntu /bin/bash`
* Terminal interativo: `docker container exec -it ID top`
* Background -> foreground: `docker container attach ID`

## IMAGE UBUNTU - SSH
* `docker pull rastasheep/ubuntu-sshd`

## IMAGE NGINX
* `docker pull nginx`
* `docker container run --publish 8080:80 nginx` ou `docker container run -p 8080:80 nginx`
* Detach/Background: `docker container run -p 8080:80 -d nginx`

