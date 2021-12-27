# docker

## Aprendo a configurar e usar o docker


## Comandos docker
#### Subir todos os containers
* ```docker-compose up```
#### Parar um container
* ```docker container stop <nome do container>``` Obs: pode usar start, stop  para iniciar e parar
#### Acessar terminal do container desejado
* ```docker exec -it <nome do container> bash```
#### Comando para restaurar DB mysql
* ```mysql -u <usuário> -p <após o enter pedirá a senha> <nome do banco> < file.sql```
#### Comando para restaurar DB mongo
* ```mongorestore --verbose <nome do arquivo>``` Obs: esse comando criará tudo que tem no arquivo, ou seja, será criado as coleções e os documentos.

#### Ativar htaccess no terminal do container do app
* Acessa o terminal do app e executa ```sudo a2enmod rewrite``` e ```sudo service apache2 restart``` Obs: Pode ser que não precise do ```sudo```
