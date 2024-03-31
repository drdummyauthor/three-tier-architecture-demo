FROM node:16

ENV INSTANA_AUTO_PROFILE true

ENV NEW_RELIC_LICENSE_KEY=
ENV NEW_RELIC_APP_NAME=UserMS
ENV NEW_RELIC_NO_CONFIG_FILE=true
ENV NEW_RELIC_DISTRIBUTED_TRACING_ENABLED=true
ENV NEW_RELIC_LOG=stdout

EXPOSE 8080

WORKDIR /opt/server

COPY package.json /opt/server/

RUN npm install

COPY server.js /opt/server/

CMD ["node", "-r", "newrelic", "server.js"]
