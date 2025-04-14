### Starting Minikube with NVIDIA GPU Support

To start Minikube with NVIDIA GPU support, use the following command:

```bash
minikube start --driver docker --container-runtime docker --gpus all
```

For more detailed information, please refer to the official Minikube NVIDIA tutorial at: https://minikube.sigs.k8s.io/docs/tutorials/nvidia/