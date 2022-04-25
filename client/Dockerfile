FROM node:lts-slim

RUN mkdir -p /usr/src/app/
WORKDIR /usr/src/app/

COPY . /usr/src/app/

RUN yarn install
RUN yarn build
RUN yarn global add serve

EXPOSE 3000

CMD ["serve", "-s", "/usr/src/app/build/"]                     