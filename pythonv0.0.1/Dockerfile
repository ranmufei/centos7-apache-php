FROM piuma/centos7-apache-php:latest

MAINTAINER Piuma <piuma@piumalab.org>

#
# Import the Centos-6 RPM GPG key to prevent warnings and Add EPEL Repository
#


RUN yum -y install \   
    python-pip \
    && yum -y update bash \
    && rm -rf /var/cache/yum/* \
    && yum clean all

RUN pip install \
    requests \
    urllib \
    bs4


ADD run.sh /


EXPOSE 80 443

CMD /run.sh
