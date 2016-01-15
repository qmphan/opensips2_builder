FROM debian:8

MAINTAINER Minh Phan <mphan@wengo.com>

RUN apt-get update
RUN apt-get install -y git vim pkg-config bison flex libjson-c-dev libxml2-dev libncurses5-dev gcc automake autoconf libcurl4-gnutls-dev libgnutls28-dev libpq-dev
########


#----------------- NGINX configuration ----------------
RUN cd /usr/local/src; git clone -b 2.1 https://github.com/OpenSIPS/opensips.git opensips2.1
RUN ADD Makefile.conf /usr/local/src/opensips2.1/Makefile.conf
RUN cd /usr/local/src; make all; make install prefix=/usr/local/opensips2


