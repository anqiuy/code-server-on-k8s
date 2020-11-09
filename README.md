# Setup code-server on kubernetes

```
HTTP_PROXY=http://<user>:<password>@<host>:<port>/
PASSWORD="<password>"
sed -e "s;%HTTP_PROXY%;$HTTP_PROXY;g" -e "s;%PASSWORD%;$PASSWORD;g" code-server-deployment.yaml
kubectl apply -f ./
