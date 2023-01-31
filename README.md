K8S
#connect instance
## Installing docker on Linux

    sudo su

    sudo apt update

    sudo apt-get install docker.io

### To check if Docker was installed properly 

    docker version
### To run Docker

    sudo systemctl enable docker

    sudo systemctl status docker

## Creating a cluster using KinD
### Install Kind on Linux - 

    curl -Lo ./kind https://kind.sigs.k8s.io/dl/v0.14.0/kind-linux-amd64

    chmod +x ./kind

    sudo mv ./kind /bin/kind

    sudo kind create cluster
### Installing kubectl
    sudo snap install kubectl

    sudo snap install kubectl --classic

### Checking the status of the cluster
    kubectl get nodes

### Pulling my docker image to store it locally

    docker pull khushichhillar/mydocker:1.0

### Loading this image using kind
    kind load docker-image khushichhillar/mydocker:1.0

