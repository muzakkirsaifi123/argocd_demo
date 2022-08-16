#### Commands

```bash
# install ArgoCD in k8s
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml

# access ArgoCD UI
kubectl get svc -n argocd
kubectl port-forward svc/argocd-server 8080:443 -n argocd

# login with admin user and below token (as in documentation):
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 --decode && echo

# you can change and delete init password

```
</br>

#### Links

* Config repo: [https://gitlab.com/nanuchi/argocd-app-config](https://gitlab.com/nanuchi/argocd-app-config)

* Docker repo: [https://hub.docker.com/repository/docker/nanajanashia/argocd-app](https://hub.docker.com/repository/docker/nanajanashia/argocd-app)

* Install ArgoCD: [https://argo-cd.readthedocs.io/en/stable/getting_started/#1-install-argo-cd](https://argo-cd.readthedocs.io/en/stable/getting_started/#1-install-argo-cd)

* Login to ArgoCD: [https://argo-cd.readthedocs.io/en/stable/getting_started/#4-login-using-the-cli](https://argo-cd.readthedocs.io/en/stable/getting_started/#4-login-using-the-cli)

* ArgoCD Configuration: [https://argo-cd.readthedocs.io/en/stable/operator-manual/declarative-setup/](https://argo-cd.readthedocs.io/en/stable/operator-manual/declarative-setup/)





######################################################################################3
minikube start 
 minikube status
 kubectl get ns
 kubectl delete ns argocd
 kubectl get ns
 watch kubectl get ns
 kubectl create namespace argocd\n
 kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml\n
 exit
 kubectl get pods -n argocd
 kubectl get pods -n argocd -w
 kubectl get all -n argocd 
 exit
 kubectl get svc -n argocd
 kubectl port-forward svc/argocd-server -n argocd 8080:443\n
 sudo systemctl stop splunk.service
 kubectl port-forward svc/argocd-server -n argocd 8080:443\n
 kubectl get secret  argocd-intial-admin-secret -n argocd -o yaml
 kubectl get secret  argocd-initial-admin-secret -n argocd -o yaml
 echo ZW5YY3VyRzN4VnJHb21qdQ== | base64 --decode