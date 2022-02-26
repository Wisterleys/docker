# docker

## Aprendo a configurar e usar o docker


## Comandos docker
#### Subir todos os containers
* ```docker-compose up```
#### Comando para listar todos o containers
* ```docker ps -a```
#### Parar um container
* ```docker container stop <nome do container>``` Obs: pode usar start, stop  para iniciar e parar
#### Acessar terminal do container desejado
* ```docker exec -it <nome do container> bash```
* #### Comando para copiar arquivo para um container docker
* ```docker cp <nome do arquivo> <nome do cotainer>:/<aqui coloca o target para jogar o arquivo>```
* #### Comando para copiar arquivo dentro de um container escolhido
* ```docker cp <nome ou id do container>:/<path para localização do arquivo> <path para cuspir o arquivo no host> exemplo: docker cp 1b4a:/out_read.jpg .```
#### Comando para restaurar DB mysql
* ```mysql -u <usuário> -p <após o enter pedirá a senha> <nome do banco> < file.sql```
#### Comando para backup DB mysql
* ```mysqldump -u <usuário> -p <após o enter pedirá a senha> <nome do banco> > file.sql```
#### Comando para restaurar DB mongo
* ```'mongorestore --archive' < db.dump``` Obs: esse comando criará tudo que tem no arquivo, ou seja, será criado as coleções e os documentos.
#### Comando para backup DB mongo
* ```mongodump --out "nomedoarquivo.dump"```

#### Ativar htaccess no terminal do container do app
* Acessa o terminal do app e executa ```sudo a2enmod rewrite``` e ```sudo service apache2 restart``` Obs: Pode ser que não precise do ```sudo```

# Atenção especial para DOCKER
#### ARemovendo todos os objetos do Docker não usados
* O ```docker system prune ``` comando remove todos os contêineres parados, imagens pendentes e redes não utilizadas 
* Use a opção -f( --force) para ignorar o prompt.

* Se você deseja remover todas as imagens não utilizadas, não apenas as pendentes, adicione a opção -a( --all) ao comando:
* ```docker system prune -a```
* Por padrão, o comando não remove volumes não utilizados para evitar a perda de dados importantes. Para remover todos os volumes não utilizados, passe a --volumesopção:
* ```docker system prune --volumes```
* ```docker system prune --volumes -f -a``` remove TODOS os volumes não utilizados
* mais informações https://linuxize.com/post/how-to-remove-docker-images-containers-volumes-and-networks/#:~:text=Stop%20and%20remove%20all%20containers,-To%20stop%20all&text=The%20command%20docker%20container%20ls,by%20the%20containers%20ID%20list.
