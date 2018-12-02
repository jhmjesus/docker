FROM ubuntu

RUN apt-get update
RUN apt-get install -y nodejs npm

RUN npm install express-generator -g

RUN mkdir /opt/app
RUN cd /opt/app

WORKDIR /opt/app

COPY ./app/app.js /opt/app/
COPY ./app/package.json /opt/app/

RUN npm install

EXPOSE 8080

CMD [ "npm", "start" ]
