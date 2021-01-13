ARG PHP_VERSION=""
FROM php:${PHP_VERSION:+${PHP_VERSION}}


RUN apk update; \
    apk upgrade;

RUN docker-php-ext-install mysqli
