#stage 1 for building
FROM node:latest as node
WORKDIR /app
COPY . .
RUN npm install
RUN npm run build --prod
#stage 2 for deploy/production
FROM nginx:alpine
COPY /dist/issue-tracker-web /usr/share/nginx/html