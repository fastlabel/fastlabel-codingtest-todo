FROM node:18.17.0-slim

RUN apt-get update; \
    apt-get install -y --no-install-recommends

WORKDIR /usr/src/front

COPY package.json ./
COPY package-lock.json ./

RUN npm install

COPY . .

EXPOSE 3000

CMD ["npm", "run", "start"]