# docker-mysql-5.7-aarch64
mysql 5.7 for docker aarch64


版本：`5.7.31`


构建：`docker build -t mysql-arm64:5.7 .`


使用方法与官方mysql镜像相同，支持`MYSQL_ROOT_PASSWORD`,`MYSQL_DATABASE`, `MYSQL_USER`,`MYSQL_PASSWORD`等环境变量配置和命令行参数


demo docker-compose.yml:
```
version: '3.8'

services:
  mysql:
    image: mysql-arm64:5.7
    container_name: mysql
    restart: always
    volumes:
      - ./mysql/data:/var/lib/mysql
    environment:
      - MYSQL_ROOT_PASSWORD=root
      - MYSQL_DATABASE=mydb
      - MYSQL_USER=myuser
      - MYSQL_PASSWORD=mypasswd
```
