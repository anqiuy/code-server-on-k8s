# Setup code-server on kubernetes

```
HTTP_PROXY=http://<user>:<password>@<host>:<port>/
PASSWORD="<password>"
TRAEFIK_NODE=<hostname>
DOMAIN=<domain>
sed -e "s;%HTTP_PROXY%;$HTTP_PROXY;g" -e "s;%PASSWORD%;$PASSWORD;g" -e "s;%TRAEFIK_NODE%;$TRAEFIK_NODE;g" -e "s;%DOMAIN%;$DOMAIN;g" *.yaml |\
kubectl apply -f -
```
