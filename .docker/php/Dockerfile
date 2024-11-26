FROM dockware/dev:latest

LABEL maintainer="Osiozekhai Aliu"
USER root
RUN curl -SsL https://github.com/boxboat/fixuid/releases/download/v0.6.0/fixuid-0.6.0-linux-amd64.tar.gz | tar -C /usr/local/bin -xzf -
RUN chmod 4755 /usr/local/bin/fixuid
RUN mkdir -p /etc/fixuid
RUN printf "user: www-data\ngroup: www-data\n" > /etc/fixuid/config.yml
RUN chmod +x /usr/local/bin/*

USER www-data:www-data