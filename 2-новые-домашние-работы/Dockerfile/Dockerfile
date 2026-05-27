# BASE IMAGE
FROM ubuntu:22.04

### MAINTAINER 
MAINTAINER devops_student

### Обновите систему и установите пакеты.
RUN apt-get update && apt-get install -y \
    nginx \
    mysql-server \
    curl \
    && rm -rf /var/lib/apt/lists/*

### Dir
WORKDIR /app

### Variáveis de ambiente
ENV APP_ENV=dev
ENV DB_NAME=school

### Copiar ficheiros da app
COPY web/index.html /var/www/html/index.html

### Adicionar script SQL
ADD init.sql /init.sql

### Create volume 
VOLUME ["/var/lib/mysql"]

### Create user non-root
RUN useradd -m devuser

USER devuser

### Gate do nginx
EXPOSE 80 3306

# Inicialização (nginx + mysql)
CMD service mysql start && \
nginx -g "daemon off;"
