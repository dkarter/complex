# Course Material

## Complex App
REALLY COMPLEX CRAZY app — for multi container deployment

---

### Setup

Apply all services and pods:

```bash
kubectl apply -f k8s
```

Set up Kubernetes Ingress Nginx

```bash
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.2.0/deploy/static/provider/cloud/deploy.yaml
```

Then visit https://localhost to view the app

### Setting up K8s dashboard (w/ Docker Desktop on macOS):
https://kubernetes.io/docs/tasks/access-application-cluster/web-ui-dashboard/#deploying-the-dashboard-ui
https://github.com/kubernetes/dashboard/blob/master/docs/user/access-control/creating-sample-user.md

