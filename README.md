# kube-ingress
ingress lab

Firstly , create a kubernetes cluster
Go to nginx official documentation and make sure Docker Login and create a private repo named dockerhub-username/nginx-ingress in your docker hub registry.
Then run kubectl apply blah blah like common/sa-and-ns.yaml ( don't forget to create NodePort for nginx-controller)
Check kubectl get all -n nginx-ingress ( if nginx-controller pods are running)
create a haproxy LB with centos vm ( as shown in Venkatls No.31 videos )

1. kubectl create -f nginx-deploy-svc-ingress-red.yaml
2. kubectl create -f nginx-deploy-blue.yaml
3. kubectl create -f nginx-svc-ingress-blue.yaml
4. and green like blue

Don't forget to add haproxy ip in /etc/hosts of each node .
