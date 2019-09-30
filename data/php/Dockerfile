FROM php:7.2-fpm
RUN apt-get update && apt-get install -y \
    git \
    && docker-php-ext-install pdo_mysql && docker-php-ext-enable pdo_mysql \
    && curl -sS https://getcomposer.org/installer | php && mv composer.phar /usr/local/bin/composer