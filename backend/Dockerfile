FROM node:20

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

## Kept running into an error with "sh: 1: nodemon: Permission denied"
## Found solution here: https://stackoverflow.com/questions/62879677/nodemon-on-docker-container-gets-permission-denied
RUN chmod +x ./node_modules/.bin/nodemon
RUN chmod +x ./node_modules/nodemon

EXPOSE 8800

CMD [ "npm", "start" ]