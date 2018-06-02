# mysql.md

1) 
docker \
  run \
  --detach \
  --env MYSQL_ALLOW_EMPTY_PASSWORD=true \
  --env MYSQL_ROOT_PASSWORD=password \
  --env MYSQL_USER=user \
  --env MYSQL_PASSWORD=user-password! \
  --env MYSQL_DATABASE=userdb \
  --name mysql \
  --publish 3306:3306 \
  mysql;

2)
docker run -d -p 3306:3306 -e MYSQL_ALLOW_EMPTY_PASSWORD=true --name mysql mysql:latest

3)
docker run -d -p 3306:3306 -e MYSQL_ROOT_PASSWORD=password --name mysql mysql:latest

## docker-compose

- docker-compose.yml

~~~yml
version: '3.4'
services:
  db:
    image: mysql:latest
    container_name: mysql
    ports:
      - "3306:3306"
#    restart: always
    environment:
      - MYSQL_ALLOW_EMPTY_PASSWORD=true | false
      - MYSQL_ROOT_PASSWORD=password
      - MYSQL_USER=root
      - MYSQL_PASSWORD=password
      - MYSQL_DATABASE=dbname
~~~
