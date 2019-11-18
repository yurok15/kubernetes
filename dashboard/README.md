kubectl apply -f recommended.yaml 
kubectl apply -f admin.user.yaml 
kubectl apply -f cluster-role-bindings.yaml 
kubectl -n kubernetes-dashboard describe secret $(kubectl -n kubernetes-dashboard get secret | grep admin-user | awk '{print $1}')
