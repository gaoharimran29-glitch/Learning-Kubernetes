# Learning-Kubernetes
Pre-requisites:- Install docker, minikube, kubectl
Check installed or not:
```bash
minikube version
kubectl version --client
docker --version
```
# Deploying a nginx page using minikube
1. Create a cluster using minikube
```bash
minikube start
```
2. Check cluster
```bash
kubectl get nodes
```
3. Create deployment
```bash
kubectl create deployment hello --image=nginx
```
Check:
```bash
kubectl get nodes
kubectl get deployments
```
4. Expose the app
```bash
kubectl expose deployment hello --type=NodePort --port=80
minikube service hello
```
