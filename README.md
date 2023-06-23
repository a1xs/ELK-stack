# ECK Operator Helm Chart

## Install elastic-operator

```shell
helm repo add elastic https://helm.elastic.co 
```
```shell
helm install elastic-operator elastic/eck-operator -n elastic-system --create-namespace
```

custom repo
```shell
cd .../ELK-stack
```
```shell
helm repo add NAME YOUR_REGISTRY
```
```shell
helm install elastic-operator codeinside/eck-operator -f values.yaml -n elastic-system --create-namespace
```

## Install ELK

```shell
cd .../ELK-stack
```
```shell
kubectl apply -f elk.yaml
```

## Remove ELK

```shell
cd .../ELK-stack
```
```shell
kubectl delete -f elk.yaml
```

## Test UDP port 
#### Example
```shell
echo "Message sent to using UDP" | nc -u k8s.DOMAIN.dmz 30005
```