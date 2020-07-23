1. Pods watch
    $ kubectl get pods --namespace cisco --watch
    
2. Get all pods for a name space
    $ kubectl get pods --namespace cisco
    $ kubectl get pods -n kube-system
    $ kubectl get pods -n cisco
    
3. Get pod logs
    $ kubectl logs kubernetes-dashboard-f8bcbd8b9-jp5z2 -n kube-system
    $ kubectl logs -n cisco action-orchestrator-pers-kafka-ha-0
    $ kubectl logs -n cisco action-orchestrator-pers-kafka-ha-0 -f
    
4. Delete one pod
    $ kubectl delete pod -n cisco action-orchestrator-pers-kafka-ha-1
    
5. Descripe service
    $ kubectl describe svc -n kube-system
    $ kubectl describe svc -n cisco
    
6. Purge/Delete AO install from local
    $ helm del --purge action-orchestrator
    
7. Get list of available name spaces
    $ helm ls
    
8. To get wide details of pods with ip and port
    $ kubectl get svc -o wide -n cisco
