# Hello Node Experiment

https://kubernetes.io/docs/tutorials/stateless-application/hello-minikube

Created Server.js

Test out starting server:

```shell
node server.js
```

Created Dockerfile


```shell
eval $(minikube docker-env)
```

```shell
docker build -t hello-node:v1 .
```

## Running

```shell
kubectl run hello-node --image=hello-node:v1 --port=8080
```

```shell
kubectl get deployments
```

```shell
kubectl get pods
```

```shell
kubectl get events
```

## Exposing

```shell
kubectl expose deployment hello-node --type=LoadBalancer
```

```shell
kubectl get services
```

```shell
minikube service hello-node
```

```shell
kubectl logs hello-node
```
