FROM php:7.1-cli
ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update \
  && apt-get install -y git mysql-server mysql-client libmysqlclient-dev --no-install-recommends \
  && docker-php-ext-install pdo pdo_mysql \
  && apt-get clean \
  && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

# This Dockerfile doesn't need to have an entrypoint and a command
# as Bitbucket Pipelines will overwrite it with a bash script.
