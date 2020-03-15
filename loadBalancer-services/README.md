Verificate cluster services type LoadBalancer
----------------------------------------------
kubetcl -n testing get srv

kubectl -n testing apply -f wordpress-service-loadbalancer


Verificate cluster service type ClusterIP
-------------------------------------------------
kubectl -n teting wordpress-service-clusterIP.yaml


