FROM node:21-alpine AS base

RUN mkdir -p /app

COPY . /app

WORKDIR /app 

RUN npm install --production

RUN npm run build 

CMD ["npm", "run", "start"]