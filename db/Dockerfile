FROM debian:wheezy

RUN apt-get update && apt-get -y upgrade
RUN apt-get install -y mysql-server

ADD mysql-listen-all.cnf /etc/mysql/conf.d/mysql-listen-all.cnf
ADD start /start
ADD pass /pass

EXPOSE 3306

CMD ["/bin/bash", "/start"]
