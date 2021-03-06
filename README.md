Install KIND (https://kind.sigs.k8s.io/docs/user/quick-start/)
----------------------------------------
curl -Lo ./kind https://kind.sigs.k8s.io/dl/v0.8.1/kind-linux-amd64

chmod +x ./kind

create cluster with two nodes
----------------------------------------
./kind create cluster --config kind-multi-node.yaml


Use cluster
------------------------------------
kubectl cluster-info --context kind-kind


Get nodes informations
---------------------------------------------
kubectl get nodes - o wide


Create a new namespace ("Testing")
-----------------------------------------------
kubectl apply -f kubernetes/namespace.yaml

Verify namespace
---------------------------------------------
kubectl get namespace


Create Nodeport in a namespace
------------------------------------------------------
kubectl -n testing apply -f kubernetes/wordpress-service.yaml


Create Replication Controller
--------------------------------------------------
kubectl -n testing apply -f kubernetes/wordpress-replication-controler.yaml 


Verify get node and test cluster access
----------------------------------------------
kubectl -n testing get node -o wide
