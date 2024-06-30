# Deployment for Clickhouse & Superset



1. Deploy superset 

```
kubectl apply -f superset.yaml
```

2. Use minikube to get the superset url
```
minikube service superset --url
```
3. Paste the URL in the browser

4. Get the superset pod name 
```
kubectl get pods
```

5. Setup username and password in superset

```
kubectl exec -it <podname> -- /bin/bash
```

6. Inside the pod run the following commands
```
superset fab create-admin
```

After setting up username and password initialize db
'''
superset db upgrade
'''
