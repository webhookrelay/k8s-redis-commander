# Redis maintenance on Kubernetes

Prerequisites:
* Kubernetes & `kubectl`
* Relay ingress controller - https://webhookrelay.com/v1/examples/relay-ingress.html
* Redis


## Clone this repo

```
git clone
```


## Deploy Redis (optional, skip if you already have one)

```
kubectl apply -f redis.yaml
```

## Deploy ingress controller


```
relay ingress init
```

## Deploy Redis Commander

1. Edit ingress definition with your custom webrelay hostname

2. Deploy it

```
kubectl apply -f redis-commander.yaml
```