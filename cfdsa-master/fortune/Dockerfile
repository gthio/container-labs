FROM node:latest

ENV APP_PORT=5000 APP_DIR=/fortune 

WORKDIR ${APP_DIR}

ADD main.js .
ADD package.json .
ADD public public
ADD views views

RUN npm install

HEALTHCHECK --interval=30s --timeout=30s --start-period=5s --retries=3 \
    CMD curl -f -s http://localhost:${APP_PORT}/health || exit 1

ENTRYPOINT [ "node", "main.js" ]


