FROM alpine
MAINTAINER Louis Bellet

# Kaigara setup
ADD operations /opt/provision/operations
ADD resources /opt/provision/resources
ADD metadata.yml /opt/provision

ADD kaigara /usr/local/bin/
ADD uhttpd /usr/local/bin/

EXPOSE 9090

VOLUME ["/var/lib/uhttpd", "/etc/uhttpd"]

ENTRYPOINT ["kaigara"]

CMD ["start", "uhttpd"]
