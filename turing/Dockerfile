FROM rust:1.81.0 AS base

RUN mkdir -p /usr/src/app 

WORKDIR /usr/src/app

COPY . .

RUN apt-get update \
	&& apt-get install --yes lcov

RUN curl -L https://foundry.paradigm.xyz | bash

RUN bash -c "source /root/.bashrc && foundryup"
