FROM node:lts-slim

ARG PORT=5000
ARG RETAIL_URL=https://example.retailcrm.ru
ARG API_KEY=""
ARG MAX_CONCURRENT_REQUESTS=5

ENV API_KEY="${API_KEY}"
ENV PORT="${PORT}"
ENV RETAIL_URL="${RETAIL_URL}"
ENV MAX_CONCURRENT_REQUESTS="${MAX_CONCURRENT_REQUESTS}"

RUN mkdir -p /usr/src/app/
WORKDIR /usr/src/app/

COPY . /usr/src/app/

RUN yarn install
RUN yarn build

EXPOSE 5000

CMD ["yarn", "start"]                     