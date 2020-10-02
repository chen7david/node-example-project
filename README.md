# node-example-project

### Dockerizing your Node App
#### Dockerfile

```dockerfile
FROM node:12

# Create app directory
WORKDIR /usr/src/app

COPY package*.json ./

RUN npm install

COPY . .

EXPOSE 8000
CMD [ "node", "./src/index.js" ]
```