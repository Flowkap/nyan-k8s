# Nyan cat for K8s

This repo shows of the difference in deploying manually by K8s manifests and by helm.
For doing so it deploys the awesome nyan cat (https://github.com/cristurm/nyan-cat) to K8s :)

## manifests

Contains manual manifests. Just deploy by e.g.:

```
cd manifests
kubectl create ns nyan
kubectl apply -f .
```

## Helm

Contains a helm chart to deploy nyan cat:

```
cd helm/nyan
kubectl create ns nyan
helm install nyan .
```

## Access

In both scenarios you can access it on your cluster via ```http(s)://<domain>/nyan``` in your browser
