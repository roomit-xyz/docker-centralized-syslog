#
# Created : Dwiyan 
#
# Maintenance : github.com/luneareth


FROM centos:7

MAINTAINER Dwiyan 

LABEL org.label-schema.person = "Dwiyan" \
      org.label-schema.name = "Syslog-NG" \
      org.label-schema.version = "3.6.XX" \
      org.label-schema.build-date = "2018-08-29"

RUN yum install -y epel-release && yum install -y syslog-ng net-tools
RUN sed -i 's/system()/# system()/g' /etc/syslog-ng/syslog-ng.conf
RUN echo '@include "/etc/syslog-ng/conf.d/networks/*.conf"' >> /etc/syslog-ng/syslog-ng.conf
RUN echo '@include "/etc/syslog-ng/conf.d/os/*.conf"' >> /etc/syslog-ng/syslog-ng.conf

VOLUME ["/docker/conf.d/networks",  "/etc/syslog-ng/conf.d/networks"]
VOLUME ["/docker/conf.d/os",  "/etc/syslog-ng/conf.d/os"]


ENTRYPOINT ["/usr/sbin/syslog-ng","--no-caps","-F"]
