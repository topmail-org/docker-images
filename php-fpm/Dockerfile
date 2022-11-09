FROM php:8.1-fpm-alpine

RUN apk add --no-cache openssh-client git

COPY --from=mlocati/php-extension-installer /usr/bin/install-php-extensions /usr/bin/install-php-extensions
COPY --from=composer:2 /usr/bin/composer /usr/bin/composer

RUN install-php-extensions \
        bcmath \
        sockets \
        pdo_mysql \
        mysqli \
        zip \
        opcache \
        pcntl \
        xsl \
        intl \
        redis
