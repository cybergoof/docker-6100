FROM ubuntu
MAINTAINER blaize.net

ADD build.sh /build.sh
RUN chmod +x /build.sh
RUN /bin/bash -c "source /build.sh"

ADD conf/nginx.conf /usr/local/nginx/conf/nginx.conf
ADD conf/modsec_includes.conf /usr/local/nginx/conf/modsec_includes.conf
ADD conf/modsecurity.conf /usr/local/nginx/conf/modsecurity.conf
ADD conf/rules/crs-setup.conf /usr/local/nginx/conf/rules/crs-setup.conf

CMD nginx -g 'daemon off;'

EXPOSE 80