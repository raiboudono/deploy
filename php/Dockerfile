FROM php:7.4-fpm

RUN set -eux \
    && apt-get update \
    && apt-get install -y --no-install-recommends \
    libzip-dev \
    && apt-get -y clean

# PHP 拡張
RUN set -eux \
    # && pecl install xdebug \
    # && docker-php-ext-enable xdebug \
    # && docker-php-ext-configure opcache --enable-opcache \
    && docker-php-ext-install \
    # opcache \
    # pdo_mysql \
    zip

WORKDIR /var/www/html
# COPY ./php.ini /usr/local/etc/php/php.ini
# COPY ./composer.* /var/www/html
# COPY --from=composer:latest /usr/bin/composer /usr/bin/composer


# install しても vendor とかが存在しない
# RUN composer install
# RUN composer dump-autoload