# 원본
* https://github.com/prometheus-community/helm-charts/tree/main/charts/kube-prometheus-stack

# 준비
* helm dependency update를 위한 helm주소 추가
```sh
helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
helm repo add kube-state-metrics https://kubernetes.github.io/kube-state-metrics
helm repo add grafana https://grafana.github.io/helm-charts
helm repo update
```