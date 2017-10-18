---
layout: single
title:  "Deploy to Minikube"
sidebar:
  nav: deploy
---



In this option you will test k8guard against a minikube context and will also deploy it to minikube. (safest way for development)

## Setup and Start Minikube
1. Install [Minikube](https://github.com/kubernetes/minikube/releases/tag/v0.20.0)

1. Start Minikube (with kubernetes v1.6.4)
```
minikube start --memory 4096 --kubernetes-version v1.6.4
```

* To try k8guard with an older version Kubernetes please refer to [version compatibility matrix](/deploy/versions/).


## Build & Deploy to Minikube

###  Deploy Option 1: Run in minikube using Kafka, Zookeeper, Memcached and Cassandra

Do the following two commands in the same terminal:

1. Use minikube docker
```
eval $(minikube docker-env)
```

2. Build and deploy
 ```
 make build-deploy-minikube
 ```

###  Deploy Option 2: Run in minikube with lighter weight dependencies of Redis and Cassandra

Do the following two commands in the same terminal:

1. Use minikube docker
```
eval $(minikube docker-env)
```

2. Build and deploy
 ```
 make build-deploy-minikube-lightweight
 ```


## Try It in Browser:

Give it a couple minutes, then hit the service urls:

1. Discover-api service url:
```
minikube service k8guard-discover-service
```
1. Report service url:
 ```
  minikube service k8guard-report-service
 ```
