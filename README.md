# Node/Express Basic Server

This is a simple node-express server to explore and understand the Immutable Server pattern.

</pr>

## Immutable Server In Action

*This setup is tough for a local configuration*

- Install https://minikube.sigs.k8s.io/docs/start/ 
- Start cluster
```bash
minikube start
```

- Point the local Docker daemon to the minikube internal Docker registry, so that minikube fetches the docker image locally
```bash
eval $(minikube -p minikube docker-env)
```

- Build Docker image and store locally
```bash
docker build . -t joanacarneiro/patterns-backend
```

- Apply kubernetes configuration
```bash
kubectl apply -f deployment.yml
```

- Verify that the pod is up and running 
```bash
kubectl get pod joanacarneiro/patterns-backend is up and running
```

***

<br>

## Testing
Postman is a useful tool to issue and save requests. Postman can create GET, PUT, POST, etc. requests complete with bodies. It can also be used to test endpoints automatically. We've included a collection (`./test_collection_postman.json `) which contains example requsts.

