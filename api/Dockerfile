FROM node:18.17.0-slim

WORKDIR /usr/src/api

RUN apt-get update && \
  apt-get install -y --no-install-recommends \
  default-mysql-client 

COPY package.json ./
COPY package-lock.json ./

RUN npm install

COPY . .

EXPOSE 4000

CMD ["/bin/sh", "entrypoint.sh"]