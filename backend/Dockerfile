FROM node:18.15.0-alpine

WORKDIR /app

COPY package*.json ./
RUN npm i

COPY . /app/

EXPOSE 3000

CMD [ "npm", "start" ]