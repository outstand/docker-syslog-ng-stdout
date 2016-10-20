# Supported tags and respective `Dockerfile` links

- [`latest`, (*Dockerfile*)](https://github.com/outstand/docker-syslog-ng-stdout/blob/master/Dockerfile)

# Usage

Add to haproxy config:
```
  log /sidecar/log local0
```

docker-compose.yml:
```yaml
version: '2'
services:
  haproxy:
    image: haproxy:latest
    volumes_from:
      - syslog-sidecar
  syslog-sidecar:
    image: outstand/syslog-ng-stdout:latest
```
