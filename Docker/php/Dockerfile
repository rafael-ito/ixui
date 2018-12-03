FROM php:7.2.12-fpm

USER root

RUN apt-get update \ 
	&& apt-get install -y apt-utils \
	&& apt-get install -y build-essential \
	&& apt-get install -y git

RUN docker-php-ext-install pdo_mysql \
    mbstring \
    mysqli

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

WORKDIR /var/www/html
