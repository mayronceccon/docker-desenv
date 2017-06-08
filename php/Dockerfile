FROM php:7.1-apache

COPY php.ini /usr/local/etc/php/

RUN apt-get update && apt-get install -y libpq-dev && docker-php-ext-install pdo pdo_pgsql
RUN apt-get update && apt-get install -y --no-install-recommends wget curl git libz-dev libmemcached-dev unzip libfreetype6-dev libjpeg62-turbo-dev libpng12-dev

#COMPOSER
RUN curl -sS https://getcomposer.org/installer | php 
RUN mv composer.phar /usr/local/bin/composer
#COMPOSER

#PHPUNIT
RUN wget https://phar.phpunit.de/phpunit.phar
RUN chmod +x phpunit.phar
RUN mv phpunit.phar /usr/local/bin/phpunit
#PHPUNIT

RUN a2enmod rewrite

RUN service apache2 restart