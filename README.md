# Sample Application Deployment

The repository contains Kubernetes manifests that defines the deployment of the
[sample application](https://github.com/gitopsbook/sample-app).

To deploy the application manually run the following command:

```
kubectl create ns sample-app
kubectl apply -f . -n sample-app
```

To test the application run the command below and access http://localhost:8080/

```
kubectl port-forward svc/sample-app 8080:80 -n sample-app
```
