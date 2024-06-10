# stars-api

# Documentação 
## Este projeto é um aplicativo Python com FastApi com todo o ambiente de execução encapsulado em Docker.

### ambiente virtual 
  python3 -m venv env


### ativação do ambiente 
  source env/bin/activate
  

### install nas dependencias 
  pip install -r requirements.txt


#### Atulização nas dependencias 
  pip freeze > requirements.txt
  

#### Comando para criar a imagem docker no projeto 
  docker build -t backoffice -f .docker/Dockerfile .


#### Configurações de vulnerabilidade da imagem sugerida pelo docker 
  docker scout cves local://backoffice:latest
  
  docker scout recommendations local://backoffice:latest


### Comando para checar se a imagem foi criada 
  docker images


### Executar o container e verificar se esta em execução 
  docker run -d -p 80:80 backoffice_soujunior
  docker ps
  

### Comandos para criar os containers 
docker-compose up 

docker-compose ps



### Comandos docker
docker-compose stop

docker-compose start 

docker-compose restart


### Porta e swagger
http://localhost:8000/docs


### Parar o servidor 
  docker stop <seu id> 65d05c5e44806478fd97914e8ecdb61a3a1b530686b20640da7c68e5717ec7a3

## Subir containers 
docker compose up

### Parar containers 
docker compose down 