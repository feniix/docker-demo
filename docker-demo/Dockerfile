FROM ubuntu:16.04

RUN \
  DEBIAN_FRONTEND=noninteractive apt-get update &&\
  DEBIAN_FRONTEND=noninteractive apt-get upgrade -y &&\
  DEBIAN_FRONTEND=noninteractive apt-get install --no-install-recommends -y apache2 &&\
  DEBIAN_FRONTEND=noninteractive apt-get clean &&\
  rm -rf /var/lib/apt/lists/*

ENV APACHE_RUN_USER www-data
ENV APACHE_RUN_GROUP www-data
ENV APACHE_LOG_DIR /var/log/apache2
ENV APACHE_LOCK_DIR /var/run

EXPOSE 80

CMD ["/usr/sbin/apache2", "-D", "FOREGROUND"]
