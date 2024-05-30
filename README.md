# Kong Gateway on k8s

```
helm install kong kong/ingress -n kong --values ./values.yaml

kubectl apply -f echo.kube.yaml       

kubectl apply -f plugin.yaml --namespace echoserver

kubectl patch ingress echoserver -p '{"metadata":{"annotations":{"konghq.com/plugins":"oidc-auth"}}}' --namespace echoserver
```

