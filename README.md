# K8s Pod Service Account

[![Artifact Hub](https://img.shields.io/endpoint?url=https://artifacthub.io/badge/repository/k8s-pod-service-account)](https://artifacthub.io/packages/search?repo=k8s-pod-service-account)

Pod service account helm package

# Sample config

```
# default config

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



