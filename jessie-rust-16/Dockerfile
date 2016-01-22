# Dockerfile
# based on https://github.com/jimmycuadra/docker-rust

FROM debian:jessie

ENV RUST_VERSION=1.6.0
ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update && apt-get install -y \
    build-essential ca-certificates curl git libssl-dev \
&&  useradd build -m -u 1000 -s /bin/bash \
&&  curl -sO https://static.rust-lang.org/dist/rust-$RUST_VERSION-x86_64-unknown-linux-gnu.tar.gz \
&&  tar -xzf rust-$RUST_VERSION-x86_64-unknown-linux-gnu.tar.gz \
&&  ./rust-$RUST_VERSION-x86_64-unknown-linux-gnu/install.sh --without=rust-docs \
&&  rm -rf rust-$RUST_VERSION-x86_64-unknown-linux-gnu \
           rust-$RUST_VERSION-x86_64-unknown-linux-gnu.tar.gz \
           /var/lib/apt/lists/* \
           /tmp/* \
           /var/tmp/*

