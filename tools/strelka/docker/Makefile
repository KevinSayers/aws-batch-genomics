NAME=strelka
TAG=2.7.1

all: build push

build:
	docker build -t $(NAME):$(TAG) -t $(NAME):latest -f Dockerfile ../..
	docker tag $(NAME):latest $(REGISTRY)/$(NAME):latest
	docker tag $(NAME):$(TAG) $(REGISTRY)/$(NAME):$(TAG)

push:
	docker push $(REGISTRY)/$(NAME):$(TAG)
	docker push $(REGISTRY)/$(NAME):latest


