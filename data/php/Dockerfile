FROM php:7.2-fpm
COPY ./sources.list /ect/apt/sources.list
RUN apt-get update && apt-get install -y \
    git \
    vim \
    iputils-ping \
    libfreetype6-dev \
    libjpeg62-turbo-dev \
    libpng-dev \
    zip \
    unzip \
    && curl -sS https://getcomposer.org/installer | php && mv composer.phar /usr/local/bin/composer \
    && composer config -g repo.packagist composer https://mirrors.aliyun.com/composer/ \
    && docker-php-ext-install pdo_mysql && docker-php-ext-enable pdo_mysql \
    && rm -r /var/lib/apt/lists/*