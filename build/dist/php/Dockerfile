ARG FROM_IMAGE=srcoder/development-php
ARG FROM_TAG=php71-fpm

FROM ${FROM_IMAGE}:${FROM_TAG}
LABEL maintainer="Jeroen Boersma <jeroen@srcode.nl>"

ARG GID=1000
ARG UID=1000

RUN echo "xdebug.mode=develop,debug" >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini
RUN groupmod -g $GID app && \
    usermod -g $GID -u $UID app
