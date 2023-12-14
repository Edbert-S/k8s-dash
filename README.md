# Kubernetes Dashboard

## Init 
```
bash script/setup
```

## Start and stop the server
```
bash script/server [start/stop]
```

## Port forwards
### K8sDash
```
kubectl proxy
```
hit this [http://localhost:8001/api/v1/namespaces/kubernetes-dashboard/services/https:kubernetes-dashboard:/proxy/#/login](url)

### Skooner
```
kubectl port-forward service/skooner 8001:8082 
```
hit this [127.0.0.1:8001](url)
The token password should be generated under token/skooner.txt
### Kubevious
```
kubectl port-forward service/kubevious-ui-clusterip -n kubevious 8002:80 
```
hit this [127.0.0.1:8002](url)