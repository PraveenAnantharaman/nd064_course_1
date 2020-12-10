Steps:

``` 
docker build -t go-helloworld .
docker run -d -p 6111:6000 go-helloworld
docker tag go-helloworld pixelpotato/go-helloworld:v1.0.0
docker push pixelpotato/go-helloworld:v1.0.0


docker login
```

deploy to Kubernetes:
```
kubectl run test --image pixelpotato/go-helloworld:v1.0.0
kubectl port-forward test-97856cf4-6fvjw 7111:6000
```
