#Base image node latest v8
FROM node:8.9.3

#Create and define directory as working directory
RUN mkdir -p /devops/app
WORKDIR /devops/app

#Copy packages from local
COPY package.json /devops/app/
COPY package-lock.json /devops/app/

#Install npm package
RUN npm install

#Copy files to working directory
COPY . /devops/app

#Port listenning
EXPOSE 8080

#Command triggered when container start
CMD ["npm", "start"]