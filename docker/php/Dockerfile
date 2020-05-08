FROM php:7.4.5-fpm-alpine3.11 as php

RUN curl -sS https://getcomposer.org/installer | php -- \
    --install-dir=/usr/local/bin \
    --filename=composer

WORKDIR /var/www/app

ENV COMPOSER_ALLOW_SUPERUSER=1
ENV COMPOSER_MEMORY_LIMIT=-1
ENV LD_PRELOAD /usr/lib/preloadable_libiconv.so php

WORKDIR /var/www/app
