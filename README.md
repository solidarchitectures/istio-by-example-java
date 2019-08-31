
# Istio by example

## Clone
```
git clone https://github.com/saturnism/istio-by-example.git
cd istio-by-example/
```

## Build
```
./mvnw clean package
```

## Docker
```
echo "$DOCKER_REGISTRY_PASSWORD" | docker login -u "$DOCKER_REGISTRY_USER" --password-stdin
```
```
cd guestbook-service/
docker build . -t bygui86/guestbook-example/guestbook-service:latest
docker push bygui86/guestbook-example/guestbook-service:latest
cd -
```
```
cd guestbook-ui/
docker build . -t bygui86/guestbook-example/guestbook-ui:1.0
docker push bygui86/guestbook-example/guestbook-ui:1.0
cd -
```
`Change background color in 'guestbook-ui/src/main/resources/templates/index.html'`
```
cd guestbook-ui/
docker build . -t bygui86/guestbook-example/guestbook-ui:2.0
docker push bygui86/guestbook-example/guestbook-ui:2.0
cd -
```
```
cd helloworld-service-java/
docker build . -t bygui86/guestbook-example/helloworld-service-java:latest
docker push bygui86/guestbook-example/helloworld-service-java:latest
cd -
```
```
cd helloworld-service-go/
docker build . -t bygui86/guestbook-example/helloworld-service-go:latest
docker push bygui86/guestbook-example/helloworld-service-go:latest
cd -
```

## Deploy
```
kubectl apply -f kubernetes-v1/
```
