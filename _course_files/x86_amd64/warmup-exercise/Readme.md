# Install Kubernetes Cluster using K3d

```
k3d cluster create istio-cluster --agents 3 -p "80:80@loadbalancer" -p "443:443@loadbalancer"
```

# CD into folder directory

```
cd istio-fleetman/_course_files/x86_amd64/warmup-exercise
```

# Install Istio Components with the following

```
kubectl apply -f ./1-istio-init.yaml
kubectl apply -f ./2-istio-minikube.yaml
kubectl apply -f ./3-kiali-secret.yaml
```

# Add istio-injection label to default namespace

```
kubectl label ns default istio-injection=enabled
```

# Install sample application

```
kubectl apply -f ./4-application-full-stack.yaml
```

# Useful links

- [fleetman-web](http://fleetman-webapp.test/)
- [kiali](http://kiali.test/)
- [jaeger](http://jaeger.test/)
