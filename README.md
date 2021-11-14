# n8n - Workflow Automation Tool

n8n is an extendable workflow automation tool and this repository is the example for run on k8s.

## Usage
create new namespace with:
 ```
 kubectl create namespace n8n
 ``` 
 
Update your config files `n8n-secrets.yml` `n8n-configmap.yaml` and `postgres-secrets.yml`

Then run all config files:
```
kubectl apply -f .
```

Local run:
```
kubectl port-forward -n n8n svc/n8n-service 8000:80 &
```

open you browser

```
http://localhost:8000/
```