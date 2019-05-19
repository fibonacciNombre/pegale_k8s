# pegale_k8s
pegale a k8s

kubectl apply -f demopegale.yml

kubectl get pods

kubectl logs pegale-6668d47cdb-2p84v

kubectl get endpoints

kubectl get pods -o wide

##kubectl apply -f ser_pegale.yml

kubectl get deployments

kubectl expose deployment pegale --type=LoadBalancer --port=80 --target-port=8080

kubectl get services

ubectl get service -w

kubectl describe service pegale

curl http://[LoadBalancer Ingress]/pegale

kubectl delete service pegale
