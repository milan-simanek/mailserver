FROM alpine:3.19

RUN apk add --no-cache \
        bash \
        ca-certificates \
        libsasl \
        mailx \
        postfix=3.8.5-r0 \
        bind-tools \
        postfix-policyd-spf-perl

RUN ln -sf /dev/stdout /var/log/mail.log

COPY run /usr/sbin/run

CMD ["/usr/sbin/run"]
