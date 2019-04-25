FROM php:7-apache
COPY php.ini /usr/local/etc/php/
RUN apt-get update \
  && apt-get install -y libfreetype6-dev libjpeg62-turbo-dev libpng-dev libmcrypt-dev git\
  && rm -rf /var/lib/apt/lists/* \
RUN git clone php7 https://github.com/phpredis/phpredis.git /usr/src/php/ext/redis\
RUN docker-php-ext-enable pdo_mysql mysqli mbstring gd iconv\
  && docker-php-ext-install pdo_mysql mysqli mbstring gd iconv\