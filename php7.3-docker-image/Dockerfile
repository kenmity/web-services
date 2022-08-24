FROM php:7.3-fpm

ADD https://github.com/mlocati/docker-php-extension-installer/releases/latest/download/install-php-extensions /usr/local/bin/
RUN chmod +x /usr/local/bin/install-php-extensions && \
    install-php-extensions igbinary msgpack imagick memcached gd mysqli memcache redis

# RUN apt-get install memcached
# RUN apt-get install php-memcached

#RUN apt-get update && apt-get install --assume-yes --no-install-recommends --quiet build-essential libmagickwand-dev
#RUN apt-get clean all
#RUN pecl install imagick && docker-php-ext-enable imagick
#RUN apt-get install -y libpq-dev
#RUN apt-get install -y zlib1g-dev libzip-dev libpng-dev
#RUN apt-get install -y libfreetype6-dev libjpeg62-turbo-dev libgd-dev
#RUN docker-php-ext-configure pgsql -with-pgsql=/usr/local/pgsql
#RUN docker-php-ext-configure gd --with-jpeg=/usr/include/ --with-freetype=/usr/include/
#RUN docker-php-ext-install gd
#RUN docker-php-ext-install zip
#RUN docker-php-ext-install mysqli pdo pdo_mysql pdo_pgsql