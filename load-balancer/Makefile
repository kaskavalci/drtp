.PHONY: run build
.DEFAULT_GOAL := run

run: build
	docker run \
		-d \
		-v `pwd`:/app/config/ \
		--restart=unless-stopped \
		-p 8082:8082 \
		lb

build:
	docker build -t lb .
