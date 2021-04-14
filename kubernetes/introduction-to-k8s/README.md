# Kubernetes basic commands

## Node / Cluster

```sh
# Check the nodes available in the cluster
kubectl get nodes
# Trivia: What happens if you try with "-o wide" option
```

## Namespace

```sh
# Get all namespaces
kubectl get ns

# Change to specific namespace where replace <name> with actual value
kubectl config set-context --current --namespace=<name>
```

## All about pods

```sh
# Show the pods only in current namespace
kubectl get po
# Trivia: What happens if you try with "-A" option
```

## All, does it really mean all

```sh
# Interestingly all doesn't show all resources
## shows pod, service, deployment, hpa, replicaset
### doesn't show ingress, secret, configmap, pv, pvc, ....read through issue - https://github.com/kubernetes/kubectl/issues/151 
kubectl get all
