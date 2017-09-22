# What is this

A general purpose dockerised gollum instance, running on alpine linux.
Adapted from https://github.com/NicolasMas/AlpineGollum

Based on the notes at: https://github.com/gollum/gollum/wiki/Gollum-via-Docker

## Installation

	docker pull mebooks/docker-gollum-alpine

## Building

	docker build -t mebooks/docker-gollum-alpine .

## Usage

	# Note that you'll need a .git folder in the host directory
	mkdir /etc/gollum && cd /etc/gollum
	git init
	docker run -v `pwd`:/wiki -p 4567:4567 mebooks/docker-gollum-alpine

	# You can specify some options
	docker run -v `pwd`:/wiki -p 4567:4567 mebooks/docker-gollum-alpine --allow-uploads --live-preview

    wget http://localhost:4567

[github.com/gollum/gollum](https://github.com/gollum/gollum#running)
