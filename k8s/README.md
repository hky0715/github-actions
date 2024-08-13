# Kubernetes Resources

## Create Base Yaml from `kubectl`

```bash
kubectl create deploy nginx-test --image=nginx -o yaml --dry-run > deployment.yaml
kubectl expose deployment nginx-test --port=80 --target-port=8000 > service.yaml
kubectl create ingress nginx-test --rule="/=nginx-test:8080" -o yaml --dry-run > ingress.yaml
```

## Deploy Test Application

* http://localhost:8080

```bash
kubectl apply -f *.yaml
```

