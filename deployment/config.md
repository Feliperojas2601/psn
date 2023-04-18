# Run to connect to gcloud cluster

```
gcloud container clusters get-credentials psn-cluster1 --zone us-east1-b
```

# Run to access your docker hub account

```
docker login --username=<username>
```

# Run to 

```
kubectl apply -f persistentVolume.yaml
kubectl apply -f persistentVolumeClaim.yaml
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
```

# Run to enter some pod and review it:

```
kubectl get pods
kubectl exec -it <nombre-del-pod> -- /bin/bash
apt-get update
apt-get install net-tools
netstat -tlnp | grep 4500
```

# Run to download nginx to the cluster

```
sudo apt-get update
curl https://raw.githubusercontent.com/helm/helm/master/scripts/get-helm-3 | bash
helm version
helm repo add nginx-stable https://helm.nginx.com/stable
helm repo update
helm install nginx-ingress nginx-stable/nginx-ingress
helm uninstall nginx-ingress
```

# Run to create a static ip

```
gcloud compute addresses create psn-ag-ip --global
```