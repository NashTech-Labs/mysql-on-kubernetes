# MySql on Kubernetes 
This template will help you to understand how to deploy mysql in kubernetes

## How to Run:
### Deploy the PV and PVC of the YAML file:
kubectl apply -f mysql-pv.yaml

kubectl apply -f mysql-pvc.yaml
### Deploy the deployment and service of the YAML file:
kubectl apply -f mysql_deployment.yaml

kubectl apply -f mysql-service.yaml
### Check if your kubernetes objects were successfully created with:
kubectl get pods

kubectl get deployments

kubectl get service
### Deploy the contents of the YAML file:
kubectl run -it --rm --image=mysql:8.0 --restart=Never mysql-client -- mysql -h mysql -ppassword
