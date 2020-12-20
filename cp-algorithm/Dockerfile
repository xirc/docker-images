FROM golang:1.15.6

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

RUN go get github.com/bazelbuild/bazelisk \
    && go get github.com/bazelbuild/buildtools/buildifier \
    && go get github.com/bazelbuild/buildtools/buildozer

ENV DEBIAN_FRONTEND=dialog