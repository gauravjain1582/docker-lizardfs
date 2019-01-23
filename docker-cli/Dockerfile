FROM ubuntu:16.04

# Install wget and busybox ( for vi )
RUN apt-get update && \
    apt-get install -y busybox gettext-base wget curl lsb-core software-properties-common 

#ENV DOCKERVERSION=18.03.1-ce

RUN curl -fsSLO https://download.docker.com/linux/static/stable/x86_64/docker-18.03.1-ce.tgz && tar xzvf docker-18.03.1-ce.tgz --strip 1 -C /usr/local/bin docker/docker  && rm docker-18.03.1-ce.tgz

COPY docker-entrypoint.sh /docker-entrypoint.sh
RUN chmod 744 /docker-entrypoint.sh

ENTRYPOINT [ "/docker-entrypoint.sh" ]
