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
For convenience, the user creation file is also available in the `extras` folder:

```bash
kubectl apply -f https://raw.githubusercontent.com/kubernetes/dashboard/v2.5.0/aio/deploy/recommended.yaml
kubectl apply -f extras
# get token (copied to clipboard):
kubectl -n kubernetes-dashboard get secret $(kubectl -n kubernetes-dashboard get sa/admin-user -o jsonpath="{.secrets[0].name}") -o go-template="{{.data.token | base64decode}}" | pbcopy
# to start the server:
kubectl proxy
```

Full instructions (which are subject to change) can be found here:
https://kubernetes.io/docs/tasks/access-application-cluster/web-ui-dashboard/#deploying-the-dashboard-ui
https://github.com/kubernetes/dashboard/blob/master/docs/user/access-control/creating-sample-user.md

