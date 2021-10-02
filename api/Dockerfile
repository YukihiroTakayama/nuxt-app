FROM ruby:3.0.1

ENV HOME="/app" \
    LANG=C.UTF-8 \
    TZ=Asia/Tokyo

RUN apt-get update -qq && \
    DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends \
    vim \
    default-mysql-client && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* && \
    truncate -s 0 /var/log/*log

WORKDIR ${HOME}
