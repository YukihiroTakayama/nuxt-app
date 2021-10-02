FROM node:10.24.0-alpine

ENV RUNTIME_PACKAGES="git" \
    HOME="/app" \
    LANG=C.UTF-8 \
    TZ=Asia/Tokyo

WORKDIR ${HOME}

RUN apk update && \
    apk upgrade && \
    apk add --update --no-cache ${RUNTIME_PACKAGES}

COPY package.json /${HOME}

RUN yarn install
