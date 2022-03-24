FROM ulsmith/alpine-apache-php7
#FROM php:7.2-apache

#COPY ./html-for-apache/index.php /var/www/index.html
COPY ./html-for-apache/index.php /app/public/index.php

EXPOSE 80
EXPOSE 8080

RUN chown -R apache:apache /app
