#base image
FROM node:latest

ENV DB_HOST=nwdb2 DB_PORT=3306 DB_USER=root DB_PASSWORD=xyz APP_PORT=3300 APP_DIR=/app

WORKDIR ${APP_DIR}

ADD main.js .
ADD package.json .
ADD config  config
ADD public public
ADD views views

RUN npm install 

EXPOSE ${APP_PORT}

ENTRYPOINT [ "node", "main.js" ]




