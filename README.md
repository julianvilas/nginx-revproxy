# nginx-revproxy
Docker image to setup a simple HTTP reverse proxy.

Required environment vars to setup the proxy:
+ `NGINX_HOST` (example: `localhost`)
+ `NGINX_PORT` (example: `80`)
+ `TARGET_URL` (example: `http://target.example.com`)

Running example:
```
$ docker run -ti --rm --name nginx -p 8080:80 -e NGINPORT=80 -e NGINX_HOST=localhost -e TARGET_URL=http://www.google.com -d redsadic/nginx-revproxy

$ curl http://localhost:8080
<!doctype html><html itemscope="" itemtype="http://schema.org/WebPage" lang="es"><head><meta content="Google...
```
