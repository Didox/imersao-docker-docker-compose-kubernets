
## Build Docker
docker build -t didox/app-imersao-docker-nodejs -f Dockerfile .

## Build Docker
docker run -d -p 80:3000 --name app-imersao-docker-nodejs didox/app-imersao-docker-nodejs

## Build watch Docker
docker run -it -p 80:3000 --name app-imersao-docker-nodejs didox/app-imersao-docker-nodejs

# Para parar o docker
docker stop app-imersao-docker-nodejs

# para remover a imagem do docker
docker rm app-imersao-docker-nodejs

# Gerar a tag da imagem no docker hub
docker tag didox/app-imersao-docker-nodejs hub.docker.com/r/didox/app-imersao-docker-nodejs

# Publicar a imagem no docker hub
docker push didox/app-imersao-docker-nodejs