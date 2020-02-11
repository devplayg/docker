FROM ubuntu:18.04

MAINTAINER devplayg <devplayg@gmail.com>

RUN sed -i s#archive\.ubuntu\.com#mirror.kakao.com#g /etc/apt/sources.list
RUN apt-get update
RUN apt-get install -y vim net-tools inetutils-ping telnet curl git
RUN curl https://dl.google.com/go/go1.13.linux-amd64.tar.gz | tar xvfz - -C /

RUN apt-get clean && \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* go1.13.linux-amd64.tar.gz

ENV GOROOT=/go
ENV GOPATH=/gohome
ENV PATH=$GOROOT/bin:$GOPATH/bin:$PATH