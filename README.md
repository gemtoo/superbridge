# Superbridge

## Proxy bridge to Internet, Tor and I2P networks

### Why does this exist?
This project is inspired by Acetone's [cross-network bridge](https://youtu.be/8r2bo-EEooM). The Dockerized version abstracts away most complexities of the guide. Currently this setup has no Yggdrasil Network support.

### How to use it?
Spin up the containers:
```
docker compose up -d
```
The proxy container binds to port 34443. Use this port as a proxy to connect to any of the mentioned networks.
```
curl -x localhost:34443 https://example.com
curl -x localhost:34443 http://i2p-site.i2p
curl -x localhost:34443 http://tor-site.onion
```