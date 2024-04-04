FROM node:16

ENV INSTANA_AUTO_PROFILE true

ENV NEW_RELIC_LICENSE_KEY=5442af596f2d6150ffd294e411fa5ef5FFFFNRAL
ENV NEW_RELIC_APP_NAME=CartMS
ENV NEW_RELIC_NO_CONFIG_FILE=true
ENV NEW_RELIC_DISTRIBUTED_TRACING_ENABLED=true
ENV NEW_RELIC_LOG=stdout

EXPOSE 8080

WORKDIR /opt/server

COPY package.json /opt/server/

RUN npm install

COPY server.js /opt/server/

CMD ["node", "-r", "newrelic", "server.js"]
