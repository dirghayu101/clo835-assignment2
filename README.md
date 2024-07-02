<<<<<<< HEAD
### Documentation:

# Getting files required
- ```wget https://raw.githubusercontent.com/sojoudian/clo835_s24/master/project-2/app.py```
- ```git init && git add . && git commit -m "setup." && git remote add origin git@github.com:dirghayu101/clo835-assignment2.git && git push -u origin main```

# Setting up docker
- ```docker system prune -a```
- ```docker build -t clo835-assignment-2 .```
- ```docker run --name clo835-assignment-2 -d -p 127.0.0.1:3030:3030 clo835-assignment-2```  <- Just for testing.
- ```docker tag clo835-assignment-2 dirghayu101/clo835-assignment-2```
- ```docker push dirghayu101/clo835-assignment-2:latest```

# Kubenetes Setup
- ```minikube start```
- ```kubectl version --client```
- ```kubectl cluster-info```

# Kubernetes Deployment
- ```kubectl apply -f deployment.yaml```
- ```kubectl apply -f service.yaml```

# Kubernetes Deployment Verification
- ```kubectl get pods -o wide```
- ```kubectl get services -o wide```
- ```kubectl get nodes```

# Kubernetes testing
- ```minikube ssh```
- ```curl <serviceIP>:<servicePort>```

# Exposing service locally
- ```minikube service clo835-assignment-2-service --url```  <- expose the services created in minikube cluster.

# Other helpful
- ```docker kill $(docker ps -q) && docker rm -f $(docker ps -a -q) #can remove f flag, or can use just the second half. ```
- ```kubectl run -i --tty --rm debug --image=busybox --restart=Never -- sh\n```
- ```kubectl get service```
- ```kubectl get pods```
- ```kubectl delete deployment <name>```
- ```kubectl delete service <name>```
- 

# References:
https://minikube.sigs.k8s.io/docs/handbook/accessing/ <- Accessing application running within minikube.
https://docs.oracle.com/en/operating-systems/olcne/1.1/orchestration/kubectl-delete.html
