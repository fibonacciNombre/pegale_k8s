# pegale_k8s
pegale a k8s

mvn clean install

docker build -f DockerFile -t demopegale .

docker run -p 8080:8080 demopegale

docker login

docker tag demopegale dingan/pegale:1

docker images

docker push dingan/pegale:1

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


-- AZURE

az acr list

"loginServer": "acr001.azurecr.io"

docker tag demopegale acr001.azurecr.io/pegale:1

az acr login -n acr001

az acr repository list -n acr001

docker push acr001.azurecr.io/pegale:1

az acr repository list -n acr001
