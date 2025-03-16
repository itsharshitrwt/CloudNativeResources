# This File is meant to demonstrate setting up tools on your local system with ease.

## Setting up Kubectl , kubernetes via minikube on wsl Ubuntu ditro

## Install kubectl
```
sudo apt update
sudo apt install -y curl
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl

```

Verify Installation

```
kubectl version --client
```
This should give 

```
Client Version: v1.32.3
Kustomize Version: v5.5.0 
```


##  Install Minikube
Since I'm on WSL Ubuntu, the best way to run Kubernetes locally is with Minikube, which will create a single-node cluster.

Setting up some dependencies

```
sudo apt update
sudo apt install -y conntrack

# better to run these commands step by step
```

Minikube Installation

```
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo install minikube-linux-amd64 /usr/local/bin/minikube

```

Check Installation

```
minikube version
```
