# Ingress Controller required the following clusterroles bindings to be applied.
```
kubectl apply -f nginx-ingress-controller.yaml
kubectl apply -f echoservice.yml
kubectl get pods,svc
kubectl create clusterrolebinding add-on-cluster-admin --clusterrole=cluster-admin --serviceaccount=kube-system:default

kubectl create clusterrolebinding add-on-cluster-admin-1 --clusterrole=cluster-admin --serviceaccount=default:default
kubectl get pods,svc
kubectl logs pod/nginx-ingress-controller-7s67s
kubectl get all
kubectl expose rc nginx-ingress-controller --type=NodePort
kubectl get svc
kubectl get pods
kubectl get pods -o wide
curl <nginx service ip>/

kubectl apply -f helloworld-v1.yml

kubectl apply -f helloworld-v2.yml
kubectl apply -f ingress-rules.yaml
kubectl get svc
kubectl get pods -o wide
kubectl describe svc helloworld-v2
curl nginxserviceip:nginxserviceport
curl nginxserviceip:nginxserviceport -H 'Host: helloworld-v1.example.com'
curl nginxserviceip:nginxserviceport -H 'Host: helloworld-v2.example.com'


```
