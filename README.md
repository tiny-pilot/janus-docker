# janus-docker

[![Docker Pulls](https://img.shields.io/docker/pulls/tinypilotkvm/janus.svg?maxAge=43200)](https://hub.docker.com/r/tinypilotkvm/janus/)
[![License](http://img.shields.io/:license-mit-blue.svg?style=flat-square)](LICENSE)

## Overview

This is a Docker image for the Janus WebRTC server.

It builds Janus specifically for use with uStreamer on a Raspberry Pi OS system, so it's probably not useful for general purpose Janus work.

## Requirements

* This must run on a Raspberry Pi device.

## Install Docker

```bash
curl -fsSL https://get.docker.com | sudo sh && \
  sudo usermod -aG docker $(whoami)
```

Log out and log in again for the docker permissions to take effect.

## Building

```bash
pushd $(mktemp -d) && \
  git clone https://github.com/tiny-pilot/janus-docker.git . && \
  docker build -t janus-ustreamer .
```
