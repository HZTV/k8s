### Задение 1

## 1.1

```
ubuntu@fhm1j15h1095nij2tpf1:~/.kube/codes$ cat netologia-pods.yml 
apiVersion: v1
kind: Pod
metadata:
  name: hello-world
spec:
  containers:
  - name: hello-world
    image: gcr.io/kubernetes-e2e-test-images/echoserver:2.2
```

## 1.2

```
ubuntu@fhm1j15h1095nij2tpf1:~$ kubectl get pod
NAME            READY   STATUS    RESTARTS   AGE
hello-world   	1/1     Running   0          30m
```

## 1.3

```
ubuntu@fhm1j15h1095nij2tpf1:~$ curl localhost:10443


Hostname: hello-world

Pod Information:
        -no pod information available-

Server values:
        server_version=nginx: 1.12.2 - lua: 10010

Request Information:
        client_address=127.0.0.1
        method=GET
        real path=/
        query=
        request_version=1.1
        request_scheme=http
        request_uri=http://localhost:8080/

Request Headers:
        accept=*/*  
        host=localhost:10443  
        user-agent=curl/7.81.0  

Request Body:
        -no body in request-
```


### Задение 2

## 2.1 2.2 2.3

```
ubuntu@fhm1j15h1095nij2tpf1:~/.kube/codes$ cat netology-web.yml 
apiVersion: v1
kind: Pod
metadata:
  name: netology-web
  labels:
    app.kubernetes.io/name: proxy
spec:
  containers:
  - name: netology-web
    image: gcr.io/kubernetes-e2e-test-images/echoserver:2.2
    ports:
      - containerPort: 80
        name: http-web-svc
        
---
apiVersion: v1
kind: Service
metadata:
  name: netology-svc
spec:
  selector:
    app.kubernetes.io/name: proxy
  ports:
  - name: name-of-service-port
    protocol: TCP
    port: 80
    targetPort: 8080
```

## 2.4

```
ubuntu@fhm1j15h1095nij2tpf1:~/.kube/codes$ curl localhost:8080

Hostname: netology-web

Pod Information:
        -no pod information available-

Server values:
        server_version=nginx: 1.12.2 - lua: 10010

Request Information:
        client_address=127.0.0.1
        method=GET
        real path=/
        query=
        request_version=1.1
        request_scheme=http
        request_uri=http://localhost:8080/

Request Headers:
        accept=*/*  
        host=localhost:8080  
        user-agent=curl/7.81.0  

Request Body:
        -no body in request-
```
