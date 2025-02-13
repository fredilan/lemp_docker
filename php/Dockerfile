FROM php:8.4-fpm

# Installing dependencies for the PHP modules
RUN apt-get update && \
    apt-get install -y zip libzip-dev libpng-dev libicu-dev curl

# Installing additional PHP modules
RUN docker-php-ext-configure intl && docker-php-ext-install mysqli pdo pdo_mysql gd pcntl zip intl

# Install Composer
COPY --from=composer:latest /usr/bin/composer /usr/local/bin/composer
