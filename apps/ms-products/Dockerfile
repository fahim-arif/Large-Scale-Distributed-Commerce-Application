# FROM node:lts-alpine
# WORKDIR /app
# COPY ./dist/apps/svc-cart .
# COPY package.json package-lock.json ./
# ENV PORT=3333
# EXPOSE ${PORT}
# RUN npm install --production
# # dependencies that express needs
# RUN npm install reflect-metadata tslib rxjs express
# CMD node ./main.js


FROM node:lts
WORKDIR /app
COPY ./dist/apps/ms-products .
COPY package.json package-lock.json ./
ENV PORT=3333
EXPOSE ${PORT}
RUN npm install --production
# dependencies that nestjs needs
RUN npm install reflect-metadata tslib rxjs @nestjs/platform-express
CMD node ./main.js

# Use official node LTS version
# FROM node:lts-alpine

# # Set working directory
# WORKDIR /app

# # Install python, make and g++ to enable building of npm packages that require it
# RUN apk add --no-cache python3 make g++

# # Copy package.json and package-lock.json
# COPY ./package.json ./
# COPY ./package-lock.json ./

# # Install dependencies
# RUN npm install --production

# # Copy built nx app to the workdir in the container
# COPY ./dist/apps/ms-products ./

# # dependencies that nestjs needs
# RUN npm install reflect-metadata tslib rxjs @nestjs/platform-express

# # Default port the app runs on
# ENV PORT=3333
# EXPOSE ${PORT}

# CMD ["node", "./main.js"]
