# K8s Pod Service Account

[![Artifact Hub](https://img.shields.io/endpoint?url=https://artifacthub.io/badge/repository/psosnicki-helm-chart-repo)](https://artifacthub.io/packages/search?repo=psosnicki-helm-chart-repo)

Pod service account helm package

# Install

## Add Repository (stable)
`$ helm repo add psosnicki-helm-repo-stable  https://psosnicki.github.io/helm3-repo/stable`   
`$ helm repo update`

## Install Package (stable)  
`$ helm install my-release psosnicki-helm-repo-stable/k8s-pod-service-account --version=1.0.0`  

# Values

```
# default values

name: "pod-service-account"

allowedResources:
  - configmaps
  - secrets

allowedVerbs:
  - get
  - list
  - watch

apiGroups:
  - ""
  - rbac.authorization.k8s.io

```
## Usage

```
serviceAccount:
  create: false
  name: "pod-service-account"
```

or set ```serviceAccountName: "pod-service-account" ``` directly in deployment.yaml



