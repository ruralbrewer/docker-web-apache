FROM php:7.2.14-fpm-alpine3.8
WORKDIR /usr/local/apache2/htdocs
RUN apk --no-cache update \
    && apk --no-cache upgrade \
    && apk add --no-cache php7-pear php7-dev php7-mysqli gcc musl-dev make
RUN docker-php-ext-install mysqli pdo_mysql \
    && pecl install redis && docker-php-ext-enable redis