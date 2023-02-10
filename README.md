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

#### can apply on running replica set
`kubectl edit replica <replica-set-name>`  
#### to scale up
`kubectl scale replicaset <replica-set-name> --replicas=5`   
