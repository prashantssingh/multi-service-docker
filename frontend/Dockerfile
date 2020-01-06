FROM       node:alpine as builder
WORKDIR    "/app"
COPY       package*.json ./
RUN        npm install 
COPY       . .
RUN        npm run build

FROM       nginx
EXPOSE     80
COPY       --from=bilder /app/build /user/share/nginx/html