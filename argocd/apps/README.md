Each folder contains an ArgoCD application, they are separate entities that can contain the same application with different customizations or unrelated applications.

## How to deploy

```sh
argocd app create free-customer-app --repo https://github.com/giovannibaratta/argocd-deploy.git --path 'argocd/apps/free-customer' --dest-namespace free-customer --dest-server https://kubernetes.default.svc --sync-policy automated
```

```sh
argocd app create premium-customer-app --repo https://github.com/giovannibaratta/argocd-deploy.git --path 'argocd/apps/premium-customer' --dest-namespace premium-customer --dest-server https://kubernetes.default.svc --sync-policy automated
```
