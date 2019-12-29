# kubernetes or k8s
## master + node
## kubernetes is useful when there is a heterogenous amount of containers running
## 'minikube' (for local machine only) only creates a cluster of nodes on local machine while 'kubectl' issues instructions inside the node created by minikube
## Installation
### install virtual box -- kubernetes works with virtulization so it needs one virtual box
### check version 'VBoxManage --version'
### install kubectl 
#### 'curl -LO https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl'
#### chmod +x ./kubectl
#### sudo mv ./kubectl /usr/local/bin/kubectl
### install minikube
#### curl -Lo minikube https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64 && chmod +x minikube
#### sudo install minikube /usr/local/bin
#### minikube version
#### minikube start
#### minikube status
#### kubectl cluster-info
## 'minikube dashboard' enable dashboard
## kubernetes uses prebuilt images, kubernetes job is only to create config
## types of kubernetes objects
### Pod -- this runs a container
### Service -- setup networking
### StatefulSet
### ReplicaController
## apiVersion: v1 -- here we can create Pod, Event, Endpoint, componentStatus, Namespace, configMap
## apiVersion: apps/v1 -- we can create ControllerRevision, StatefulSet
## kubernetes can not run a single container but instead it runs it using pods
## pods should contain the containers who can not work without each otherl, so that the entire deps is setup when a new instance is instantiated
