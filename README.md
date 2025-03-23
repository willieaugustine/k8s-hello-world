# Kubernetes Nginx Deployment

This project sets up an Nginx web server using Kubernetes. It includes a Deployment and a Service configuration to expose the application within a cluster.

## Project Structure
```
/k8s-hello-world
│── deployment.yaml   # Kubernetes Deployment configuration
│── service.yaml      # Kubernetes Service to expose Nginx
│── .gitignore        # Files to ignore in Git
│── README.md         # Project documentation
```

## Prerequisites
Ensure you have the following installed:
- [Docker](https://docs.docker.com/get-docker/)
- [Minikube](https://minikube.sigs.k8s.io/docs/start/)
- [Kubectl](https://kubernetes.io/docs/tasks/tools/)
- [Git](https://git-scm.com/)

## Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/k8s-hello-world.git
cd k8s-hello-world
```

### 2. Start Minikube (if running locally)
```bash
minikube start
```

### 3. Deploy Nginx to Kubernetes
```bash
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
```

### 4. Verify Deployment and Service
Check the pods and services:
```bash
kubectl get pods
kubectl get svc
```

### 5. Access the Application
If using Minikube:
```bash
minikube service nginx-service
```
If using a LoadBalancer or NodePort, access via:
```bash
http://<EXTERNAL_IP>:<PORT>
```

## Cleanup
To remove the deployment and service:
```bash
kubectl delete -f deployment.yaml
kubectl delete -f service.yaml
```

## Contributing
Feel free to fork and submit a pull request if you want to improve the project.

## License
This project is licensed under the MIT License.

