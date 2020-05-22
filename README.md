# ANDROID KITCHEN

![logo](https://assets.gitlab-static.net/uploads/-/system/project/avatar/12904438/android-kitchen-3.3-1.png)

## INDEX

- [ANDROID KITCHEN](#android-kitchen)
  - [INDEX](#index)
  - [BADGES](#badges)
  - [INTRODUCTION](#introduction)
  - [PREREQUISITES](#prerequisites)
  - [INSTALL](#install)
    - [DOCKER RUN](#docker-run)
    - [DOCKER COMPOSE](#docker-compose)
  - [LICENSE](#license)

## BADGES

[![pipeline status](https://gitlab.com/oda-alexandre/android-kitchen/badges/master/pipeline.svg)](https://gitlab.com/oda-alexandre/android-kitchen/commits/master)

## INTRODUCTION

Docker image of :

- [android-kitchen](https://developer.android.com/studio)

Continuous integration on :

- [gitlab pipelines](https://gitlab.com/oda-alexandre/android-kitchen/pipelines)

Automatically updated on :

- [docker hub public](https://hub.docker.com/r/alexandreoda/android-kitchen/)

## PREREQUISITES

Use [docker](https://www.docker.com)

## INSTALL

### DOCKER RUN

```\
docker run -d \
--name android-kitchen \
-v ${HOME}:/home/android-kitchen \
-v /dev/bus/usb:/dev/bus/usb \
alexandreoda/android-kitchen
```

### DOCKER COMPOSE

```yml
version: "2.0"

services:
  android-kitchen:
    container_name: android-kitchen
    image: alexandreoda/android-kitchen
    restart: "no"
    privileged: false
    volumes:
      - "${HOME}:/home/android-kitchen"
      - "/dev/bus/usb:/dev/bus/usb"
```

## LICENSE

[![GPLv3+](http://gplv3.fsf.org/gplv3-127x51.png)](https://gitlab.com/oda-alexandre/android-kitchen/blob/master/LICENSE)
