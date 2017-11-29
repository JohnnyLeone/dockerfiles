FROM alpine:latest
LABEL maintainer Andreas Hirschauer <andi@linux.com>

RUN apk --no-cache add \
        syslog-ng

ADD syslog-ng.conf /etc/syslog-ng/syslog-ng.conf

EXPOSE 514

WORKDIR /export

ENTRYPOINT [ "syslog-ng" ]
CMD [ "--process-mode=foreground", "--no-caps" ]
