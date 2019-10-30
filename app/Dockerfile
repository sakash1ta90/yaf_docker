FROM php:7.3-fpm-alpine3.8

RUN apk upgrade --update && \
  apk --no-cache add autoconf make g++ && \
  pecl install -f xdebug-2.7.0 yaf && \
  docker-php-ext-enable xdebug && \
  docker-php-ext-install pdo_mysql

COPY app/override.ini /usr/local/etc/php/conf.d/overrides.ini
