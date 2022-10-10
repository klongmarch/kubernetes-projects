source document:
https://kubernetes.io/docs/tasks/access-application-cluster/ingress-minikube/

---------------------------
when there is this error:

kubectl apply -f example-ingress.yaml 

Error from server (InternalError): error when creating "example-ingress.yaml": Internal error occurred: failed calling webhook "validate.nginx.ingress.kubernetes.io": failed to call webhook: Post "https://ingress-nginx-controller-admission.ingress-nginx.svc:443/networking/v1/ingresses?timeout=10s": dial tcp 10.100.235.186:443: connect: connection refused

Do the following:
kubectl delete -A ValidatingWebhookConfiguration ingress-nginx-admission
---------------------------

