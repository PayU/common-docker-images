FROM alpine:edge
LABEL maintainer="stefan.kiss@payu.ro"



RUN apk update \
	&& apk --no-cache -X http://nl.alpinelinux.org/alpine/edge/testing \
	add dante dante-server dante-doc

COPY sockd.conf /etc/sockd.conf
#run!
ENTRYPOINT ["/usr/sbin/sockd","-f","/etc/sockd.conf"]

