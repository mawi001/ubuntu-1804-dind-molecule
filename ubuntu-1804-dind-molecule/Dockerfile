FROM ubuntu:bionic as base

COPY prepare-docker-in-docker.yml /

RUN apt update && apt install -yqq python python-pip sudo ca-certificates unzip systemd && \
  pip install ansible==2.8.5 && \
  ansible-playbook -v prepare-docker-in-docker.yml && \
  rm -rf /var/lib/apt/lists/*
