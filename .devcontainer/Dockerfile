FROM mcr.microsoft.com/devcontainers/base:alpine-3.20
RUN set -ex; apk update \
    && apk add linux-headers openssl-dev pcre2-dev zlib-dev openssl abuild \
               musl-dev libxslt libxml2-utils make mercurial gcc unzip git \
               xz g++ coreutils curl
