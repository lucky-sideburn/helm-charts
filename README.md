# KubeInvaders Helm Chart Repository 

## Usage

```bash
helm repo add kubeinvaders https://lucky-sideburn.github.io/helm-charts/
helm repo update

kubectl create namespace kubeinvaders

helm install kubeinvaders --set-string config.target_namespace="namespace1\,namespace2" \
-n kubeinvaders kubeinvaders/kubeinvaders --set ingress.enabled=true --set ingress.hostName=kubeinvaders.io --set deployment.image.tag=v1.9.6
```

## Helm Values

| Variable            | Description                            |
| ------------------- | -------------------------------------- |
| image.tag           | Specify tag of KubeInvaders to deploy  |
| ingress.hostName    | URL used for ingress                   |
| target_namespace    | namespaces to take under control       |
