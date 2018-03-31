From ubuntu:xenial
MAINTAINER Tony Arkles

# Set noninteractive mode for apt-get
ENV DEBIAN_FRONTEND noninteractive

# Update
RUN apt-get update

# Start editing
# Install package here for cache
RUN apt-get -y install supervisor rsyslog postfix postfix-ldap sasl2-bin opendkim opendkim-tools ca-certificates

ADD scripts/install.sh /opt/install.sh

CMD /opt/install.sh;/usr/bin/supervisord -c /etc/supervisor/supervisord.conf