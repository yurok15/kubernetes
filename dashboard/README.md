kubectl apply -f recommended.yaml <br>
kubectl apply -f admin.user.yaml <br>
kubectl apply -f cluster-role-bindings.yaml <br>
kubectl -n kubernetes-dashboard describe secret $(kubectl -n kubernetes-dashboard get secret | grep admin-user | awk '{print $1}') <br>
