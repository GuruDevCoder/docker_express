FROM node:12.13.0-alpine AS base

WORKDIR /usr/src/app

# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
# where available (npm@5+)
COPY package.json ./
COPY yarn.lock ./

RUN yarn
# If you are building your code for production
# RUN npm ci --only=production

COPY ./src .

EXPOSE 8080

CMD [ "node", "server.js" ]