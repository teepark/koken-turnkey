FROM debian:wheezy

RUN apt-get update && apt-get -y upgrade
RUN apt-get install -y apache2 libapache2-mod-php5 php5-mysql php5-gd php5-curl
RUN /usr/sbin/a2enmod rewrite

ENV APACHE_RUN_USER www-data
ENV APACHE_RUN_GROUP www-data
ENV APACHE_LOG_DIR /var/log/apache2

ADD webroot/index.php /koken-install.php
ADD default /etc/apache2/sites-available/default

ADD start /start

EXPOSE 80

CMD ["/bin/sh", "/start"]
