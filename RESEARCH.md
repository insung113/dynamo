## Required Tools

The following tools are needed to run the examples and demos:

- Docker: Container runtime for building and running services
- Helm: Kubernetes package manager for deploying applications
- Minikube: Local Kubernetes environment for testing
- kubectl: Command-line tool for interacting with Kubernetes clusters
- Earthly: Build automation tool used by Dynamo for container image creation

### GitHub Container Registry Login

To access private container images from GitHub Container Registry, use the following commands:

```bash
export CR_PAT=ghp_xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
export USERNAME=username
echo $CR_PAT | docker login ghcr.io -u $USERNAME --password-stdin
```

Replace `ghp_xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx` with your GitHub Personal Access Token and `username` with your GitHub username.

### Starting Minikube with NVIDIA GPU Support

To start Minikube with NVIDIA GPU support, use the following command:

```bash
minikube start --driver docker --container-runtime docker --gpus all
```

For more detailed information, please refer to the official Minikube NVIDIA tutorial at: https://minikube.sigs.k8s.io/docs/tutorials/nvidia/