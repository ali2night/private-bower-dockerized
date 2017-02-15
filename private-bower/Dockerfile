# pull debian
FROM debian:latest
# install nodejs
RUN apt-get update && apt-get install -y curl apt-transport-https  && curl -sL https://deb.nodesource.com/setup_6.x |  bash - && \
        apt-get install -y nodejs
# install npm-cache-server
RUN npm install -g bower private-bower
# create storage directory
COPY config /config

cmd private-bower --config /config/private-bower.json
