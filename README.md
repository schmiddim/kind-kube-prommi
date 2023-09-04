# kind-kube-prommi

## Start Custer
```
kind create cluster --image kindest/node:v1.23.5
```


## Start Cluster && install KubePrometheus Stack
```
kind create cluster --image kindest/node:v1.23.5
helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
helm repo update
helm upgrade  --install kube-prometheus  prometheus-community/kube-prometheus-stack -f kube-prometheus-values.yaml 
```