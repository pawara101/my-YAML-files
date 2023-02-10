# my-YAML-files with important Kubernetes commands

## Replica Sets / Replication control

`kubectl create -f replication-controller.yaml`
`kubectl delete -f replication-controller.yaml`
`kubectl get replicationcontroller`

`kubectl create -f replica-set.yaml`
`kubectl get replicaset`

### scale and update the replica set in yaml file
`kubectl replace -f replica-set.yaml` 

### scale and update the replica set
`kubectl scale -replicas=6 -f replica-set.yaml`

`kubectl explain pod`
`kubectl explain replicaset`

*can apply on running replica set*
`kubectl edit replica <replica-set-name>`  
*to scale up*
`kubectl scale replicaset <replica-set-name> --replicas=5`   

## NameSpaces
`kubectl get pods` *gives  pods in default namespace*
`kubectl get pods --namespace=kube-system` *gives pods in another namespace*
`kubectl get pods --all-name-spaces`  *defines pods in all namespaces*

*To deploy redis in another Namespace*
`kubectl run redis --image=redis --namespace=new-ns` or `kubectl run redis --image=redis --n=new-ns`


## Labels & Selectors
`kubectl get pods --selector <label key>=<label>` *to check pods which has specific namespace*
** Example :** `kubectl get pods --selector app=App1`


## Taints and Tolerations
** Taints involve in Nodes**
**Tolerations involve with pods**
`kubectl taint node node-name key=value:taint-effect`
`kubectl taint node node-name app=blue:NoSchedule`
