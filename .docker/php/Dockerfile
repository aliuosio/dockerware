FROM dockware/dev:latest

LABEL maintainer="Osiozekhai Aliu"

USER root

RUN apt update && \
    apt upgrade -y && \
    apt install -y php-redis redis-tools && \
    curl -SsL https://github.com/boxboat/fixuid/releases/download/v0.6.0/fixuid-0.6.0-linux-amd64.tar.gz | tar -C /usr/local/bin -xzf - && \
    chmod 4755 /usr/local/bin/fixuid && \
    mkdir -p /etc/fixuid && \
    printf "user: dockware\ngroup: www-data\n" > /etc/fixuid/config.yml && \
    chmod +x /usr/local/bin/*

USER dockware