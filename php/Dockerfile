FROM php:7-fpm
RUN apt-get update && apt install -y libmemcached-dev zlib1g-dev
RUN docker-php-ext-install mysqli
RUN printf "\n" | pecl install memcached
RUN docker-php-ext-enable memcached
ADD php/php.ini /usr/local/etc/php
