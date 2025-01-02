# argocd
Commands Used in this video:
kubectl cluster-info
brew install kubectl
brew install minikube
minikube start
docker version
brew install argocd
argocd version
kubectl get nodes
kubeclt create ns argocd
kubectl get ns
Spec for ArgoCD: https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
kubectl get all -n argocd
kubectl patch svc argocd-server -n argocd -p '{"spec:" {"type": "NodePort"}}' -- command to run argocd webui, exposes nodeport
kubectl port-forward svc/argocd-server -n argo 8080:443
Run the UI: localhost:8080
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d && echo
