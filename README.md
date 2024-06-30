# Superset + Clickhouse


1. Deploy superset deployment with the below command

```
kubectl apply -f superset.yaml
```

2. Get the URL for the superset with the below command

```
minikube service superset --url
```
3. Paste the URL in the browser

4. Get the superset pod name with the below command
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
