FROM php:8.1.4-fpm

ADD php.ini /usr/local/etc/php/

RUN cd /usr/bin && curl -s http://getcomposer.org/installer | php \
   && ln -s /usr/bin/composer.phar /usr/bin/composer \
   && apt update \
   && apt install -y zip unzip libpng-dev libpq-dev \
   && curl -sL https://deb.nodesource.com/setup_12.x | bash - \
   && apt install -y nodejs \
   && docker-php-ext-install pdo_mysql
