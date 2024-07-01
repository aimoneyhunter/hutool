
kubectl -n default autoscale deployment nginx-dao2048 --cpu-percent=50 --min=3 --max=10

