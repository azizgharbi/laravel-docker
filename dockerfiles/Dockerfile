FROM php:7.1.3-fpm

RUN apt-get update
RUN apt-get install -y zlib1g-dev
RUN apt-get install -y libicu-dev
RUN apt-get install -y libpq-dev
RUN apt-get install -y libmcrypt-dev
RUN apt-get install -y mysql-client
RUN apt-get install -y libmagickcore-dev
RUN apt-get install -y libmagickwand-dev
RUN docker-php-ext-install mcrypt
RUN docker-php-ext-install mysqli
RUN docker-php-ext-install opcache
RUN docker-php-ext-install intl
RUN docker-php-ext-install mbstring
RUN docker-php-ext-install pdo_mysql
RUN docker-php-ext-install pdo_pgsql
RUN docker-php-ext-install zip
RUN docker-php-ext-install gd
RUN pecl install imagick-3.4.3
RUN docker-php-ext-enable imagick
RUN pecl install apcu-5.1.5
RUN docker-php-ext-enable apcu

WORKDIR /var/www/html