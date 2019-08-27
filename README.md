# Kubernetes-sample

This is a sample repo where I play around Kubernetes with a simple Rails application on Docker container.

## Set up

```
$ docker build -f .docker/app/Dockerfile . -t k8s-sample
$ docker run -itd --name k8s-sample-container -v `pwd`:/kubernetes-sample k8s-sample
$ docker exec -it k8s-sample-container bash
```
