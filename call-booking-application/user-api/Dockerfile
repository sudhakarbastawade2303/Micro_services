FROM node:17.9.0-slim
LABEL maintainer="sudhakar"
#adding new user because we should to run cmd with root access
RUN useradd userapi 
#setting up directory to copy code
WORKDIR /app
#copying the all codes from root[where this dockerfile is present into a /app directory]
COPY . .
#this npm install will help u to build code 
RUN npm install 
EXPOSE 1004
#setting the user to run below cmd 
USER userapi
#we need mongodb to store the user details 
ENV MONGO_URL=""
#still admin service is not ready so we will not use it 
#ENV ADMIN_EMAIL=""
#below cmd will start the node application 
CMD ["npm","start"]