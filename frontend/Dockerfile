# syntax=docker/dockerfile:1

FROM nginx:latest
ENV NODE_ENV=production

WORKDIR /app

COPY ["package.json", "./"]

RUN npm i react-scripts -g

RUN npm ci --production

COPY . .

CMD [ "npm", "start" ]