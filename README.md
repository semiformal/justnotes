# justnotes
Just some notes


## install gitan on 18.04 ubuntu
From: https://github.com/devrandom/gitian-builder
This pulls in all pre-requisites for KVM building on Ubuntu:

`sudo apt-get install git apache2 apt-cacher-ng python-vm-builder ruby qemu-utils`

If you'd like to use docker mode instead, install it as follows:

NOTE: this doesn't work right now and you need the below section
`sudo apt-get install docker-ce`

### Installing docker-ce on ubuntu
From: https://github.com/docker/for-linux/issues/290#issuecomment-393605253

```#!/usr/bin/env bash

sudo apt update

sudo apt --yes install \
    software-properties-common \
    apt-transport-https \
    ca-certificates \
    curl

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

sudo add-apt-repository \
    "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"

sudo apt update

sudo apt --yes install docker-ce

sudo usermod --append --groups docker $USER```
