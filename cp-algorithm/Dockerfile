FROM golang

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update \
    && apt-get -y install \
        build-essential \
        ca-certificates \
        clang \
        cmake \
        curl \
        git \
        gzip \
        ssh \
        tar \
    && apt-get autoremove -y \
    && apt-get clean -y \
    && rm -rf /var/lib/apt/lists/*

RUN go install github.com/bazelbuild/bazelisk@latest \
    && go install github.com/bazelbuild/buildtools/buildifier@latest \
    && go install github.com/bazelbuild/buildtools/buildozer@latest

ENV DEBIAN_FRONTEND=dialog