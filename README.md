# k8s_training

create with kubectl apply -f https://k8smastery.com/shpod.yaml
attach with kubectl attach --namespace=shpod -ti shpod
delete with kubectl delete -f https://k8smastery.com/shpod.yaml

use attach for 1st terminal
use kubectl exec --namespace=shpod -ti shpod -- bash -l
for 2nd terminal to have a new bash shell

kubectl get nodes -o json | jq ".items[] | {name:.metadata.name} + .status.capacity"
list of items in node more readable format
