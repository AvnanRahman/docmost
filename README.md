# docmost
Deployment docmost in kubernetes

Dokumentasi resminya hanya ada Docker Compose:  
https://docmost.com/docs/installation/  
https://github.com/docmost/docmost

# Create password
```
echo -n "PasswordApp" | base64
echo -n "PasswordDB" | base64
```

# Deployment
```
k apply -f namespace.yaml
k apply -f pvc.yaml
nano secret.yaml
k apply -f secret.yaml
k apply -f redis.yaml
k apply -f postgres.yaml
k apply -f docmost.yaml
```
