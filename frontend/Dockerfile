FROM node:18 AS build

WORKDIR /usr/app
COPY ./ /usr/app


RUN npm install



RUN npm run build


FROM nginx:alpine


COPY --from=build /app/build /usr/share/nginx/html

EXPOSE 80
