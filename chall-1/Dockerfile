FROM ubuntu:20.04

RUN echo "Acquire::http::Pipeline-Depth 0;" > /etc/apt/apt.conf.d/99custom && \
    echo "Acquire::http::No-Cache true;" >> /etc/apt/apt.conf.d/99custom && \
    echo "Acquire::BrokenProxy    true;" >> /etc/apt/apt.conf.d/99custom

RUN apt update
RUN apt -y install openssh-server

RUN useradd -m -s /usr/bin/bash level1

EXPOSE 22
