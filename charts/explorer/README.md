# Explorer Helm Charts
This repo contains Helm charts for the Symbol Explorer.

## Requirements
- Kubernetes(K8s) v1.25.2
  - ingress-nginx controller plugin
  ```
  kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.4.0/deploy/static/provider/cloud/deploy.yaml
  ```
- Helm v3.10.1

## Installation

### Local Deployment
To deploy Testnet Explorer to local K8s environment:
```
helm install local-explorer ./charts/explorer -f ./charts/explorer/values-local.yaml
```

### Testnet Deployment
To deploy Testnet Explorer to a Testnet K8s environment:
```
helm install testnet-explorer ./charts/explorer -f ./charts/explorer/values-testnet.yaml
```

### Mainnet Deployment
To deploy Mainnet Explorer to a Mainnet K8s environment:
```
helm install mainnet-explorer ./charts/explorer -f ./charts/explorer/values-mainnet.yaml
```

