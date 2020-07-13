FROM node:12-alpine

# Create app directory
WORKDIR /app/
COPY . .
RUN apk update && apk upgrade \
    && npm install --quiet \
    && apk add php7 php7-fpm php7-opcache php7-json php7-zlib php7-curl
RUN npm run build
CMD npm run serve