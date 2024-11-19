kubectl config get-clusters
kubectl get secret cd-token -n homework -o jsonpath='{.data.token}' | base64 --decode
kubectl config view --minify -o jsonpath='{.clusters[0].cluster.server}'
kubectl config view --raw -o jsonpath='{.clusters[0].cluster.certificate-authority-data}'
kubectl --kubeconfig=cd-kubeconfig.yaml get pods -n homework