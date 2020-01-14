FROM php:7.1.20-apache

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get -y update --fix-missing
RUN apt-get upgrade -y

# Install useful tools
RUN apt-get -y install apt-utils nano wget dialog netcat

#Install important libraries
RUN apt-get -y install --fix-missing apt-utils libxml2-dev libpng-dev zlib1g-dev poppler-utils build-essential git curl libcurl3 libcurl3-dev zip libsqlite3-dev libsqlite3-0 mysql-client

RUN docker-php-ext-install pdo_mysql
RUN docker-php-ext-install bcmath
RUN docker-php-ext-install pdo_sqlite
RUN docker-php-ext-install simplexml
RUN docker-php-ext-install mysqli
RUN docker-php-ext-install gd

RUN docker-php-ext-install curl
RUN docker-php-ext-install tokenizer
RUN docker-php-ext-install json

# Enable apache modules
RUN a2enmod rewrite headers

RUN deluser www-data \
	&& groupadd -g 1000 -r www-data \
	&& useradd -u 1000 -p -s -g www-data www-data

RUN apache2ctl restart

