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
