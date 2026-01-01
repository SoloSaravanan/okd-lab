TLS Certificates
Generate

```
openssl req -x509 -sha256 -nodes -days 365 -newkey rsa:2048 -keyout tls.key -out tls.crt -subj "/CN=localhost" -addext 'subjectAltName = IP:127.0.0.1'
```

HTTP based
```
podman play kube --configmap okd-configmap.yml pod.yml
```

The UI will available at: http://<host-ip-address>:8080
