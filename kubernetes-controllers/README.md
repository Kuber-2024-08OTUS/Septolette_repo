kubectl get nodes
kubectl label nodes <имя-ноды> homework=true
kubectl get nodes --show-labels | grep homework=true