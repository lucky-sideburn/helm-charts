# Helm Chart Repository for

* [kubeinvaders](https://github.com/lucky-sideburn/KubeInvaders)

Contributions from kubeinvaders to KubeInvaders are welcome!


## Usage

```bash
helm repo add kubeinvaders https://lucky-sideburn.github.io/helm-charts/

kubectl create namespace kubeinvaders

# Install new and full open-source version
helm install kubeinvaders --set-string target_namespace="namespace1\,namespace2" \
--namespace kubeinvaders ./helm-charts/kubeinvaders \
--set ingress.hostName=kubeinvaders.io --set image.tag=v1.0
```

## Helm Values

| Variable            | Description                            |
| ------------------- | -------------------------------------- |
| image.tag           | Specify tag of KubeInvaders to deploy  |
| ingress.hostName    | URL used for ingress                   |
| target_namespace    | namespaces to take under control       |
