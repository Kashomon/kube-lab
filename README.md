# Kube Lab

Playing around with Kubernetes!

## Notes

### Getting things running

```shell
curl -Lo minikube https://storage.googleapis.com/minikube/releases/latest/minikube-darwin-amd64 && \
  chmod +x minikube && \
  sudo mv minikube /usr/local/bin/
```

```shell
brew install docker-machine-driver-xhyve
sudo chown root:wheel $(brew --prefix)/opt/docker-machine-driver-xhyve/bin/docker-machine-driver-xhyve
sudo chmod u+s $(brew --prefix)/opt/docker-machine-driver-xhyve/bin/docker-machine-driver-xhyve
```

Already had kubectl installed via gcloud

```shell
minikube start --vm-driver=xhyve
```

```shell
kubectl config use-context minikube
```

```shell
kubectl cluster-info
```
