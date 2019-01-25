Part of example hosted here: https://blog.karmacomputing.co.uk/understanding-kubernetes/

# Create an deploy a helloWorld

### 1. Create docker image

Here's an example 'helloworld' app (guilty, yes this is a node app, based on the [Kubernetes example](https://kubernetes.io/docs/tutorials/hello-minikube/)) **but not using minikube** using [microk8s](https://tutorials.ubuntu.com/tutorial/install-a-local-kubernetes-with-microk8) instead. 

### 2. Build it
microk8s.docker build -t localhost:32000/helloworld:latest .
microk8s.docker push localhost:32000/helloworld:latest

### 3. Create a deployment
sudo microk8s.kubectl create deployment hello-world --image=127.0.0.1:32000/helloworld:latest

### 4. Create service by exposing deployment

### 5. Build it
microk8s.docker build -t localhost:32000/helloworld:latest .
microk8s.docker push localhost:32000/helloworld:latest

### 6. Create a deployment
sudo microk8s.kubectl create deployment hello-world --image=127.0.0.1:32000/helloworld:latest

### 7. Create service by exposing deployment

kubectl expose deployment hello-world --type=NodePort --port=8081
