FROM php:8.2-fpm

RUN apt-get update && apt-get install -y \
    git curl zip unzip libpng-dev libonig-dev libxml2-dev libcurl4-openssl-dev \
    libzip-dev libssl-dev libpq-dev libmcrypt-dev libjpeg-dev \
    && docker-php-ext-install pdo pdo_mysql zip mbstring exif pcntl bcmath sockets gd

COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

WORKDIR /var/www/html
