FROM node:18.14-alpine

WORKDIR /app/frontend

ENV PATH /app/node_modules/.bin:$PATH

COPY package.json /app/package.json

RUN npm install --silent

EXPOSE 3000