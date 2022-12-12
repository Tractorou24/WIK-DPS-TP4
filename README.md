# WIK-DPS-TP4

Kubernetes TP with Pods, ReplicaSet and Deployments

## Part 1

Using the file v1.yaml:
```bash
kubectl create -f .\v1.yaml
kubectl port-forward echo-server 8080:8080 
```

Then go to http://localhost:8080/ping and you should see the api response.

## Part 2

Using the file v2.yaml:
```bash
kubectl create -f .\v2.yaml
kubectl port-forward service/echo-loadbalancer 8080:8080
```
Then go to http://localhost:8080/ping and you should see the api response.

## Part 3
Using the file v3.yaml:
```bash
kubectl create -f .\v3.yaml
```
Add cppisthebest.com to /etc/hosts with the given ip and go to http://cppisthebest.com/ping and you should see the api response.

## Bonus

Go into the bonus folder and run the following commands:
```bash
kubectl apply -k .
```

On windows, run `minikube service wordpress --url` and go to the specified utl in your browser.