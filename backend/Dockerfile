From node:18-alpine
# node-18-alpine is lighter version of node:!8
WORKDIR  /app 
# this will store our code in app directory of docker container that we will make

# add here for python and all
RUN apk update && apk add --no-cache g++

COPY package.json .
RUN npm install
# COPY <local>  <container>
COPY . . 
# or-> COPY . /app
# this will copy things from our computer to container

# First. means that copy from the root directory to the DockerFile

# Second  . means  represents working directory of Container

EXPOSE 5000
CMD ["node" ,"index.js"]
