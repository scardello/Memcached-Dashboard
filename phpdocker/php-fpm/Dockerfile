FROM phpdockerio/php56-fpm:latest
WORKDIR "/application"

# Fix debconf warnings upon build
ARG DEBIAN_FRONTEND=noninteractive

# Install selected extensions and other stuff
RUN apt-get update \
    && apt-get -y --no-install-recommends install  php5-memcached \
    && apt-get -y --no-install-recommends install php-pear php5-dev \
    && apt-get -y --no-install-recommends install zlib1g zlib1g-dev build-essential \
    && pecl install memcache \
    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*    