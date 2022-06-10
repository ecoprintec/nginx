# helm-charts

## Common
```
mkdir charts && cd charts
```

## Helm Create - nginx
```
helm create nginx
```

## Deploy nginx using helm chart
```
helm upgrade nginx charts/nginx/ \
    --install \
    --namespace nginx \
    --create-namespace \
    --set replicaCount=2 \
    --set ingress.enabled=true \
    --set ingress.className=nginx
```

## Delete nginx using helm chart
```
helm uninstall nginx -n nginx
```
