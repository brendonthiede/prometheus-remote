# Prometheus Remote

This is a simple Prometheus service to be used as a remote receiver, for use with another Prometheus instance configured `remote_read`/`remote_write`. If deployed to the `prom` namespace with the default values, the remote configurations would look like:

```yaml
remote_read:
    - url: http://prometheus.prom.svc:9090/read
remote_write:
    - url: http://prometheus.prom.svc:9090/write
```

## Installation

Installation via Helm could look like:

```bash
helm upgrade --install prometheus https://github.com/brendonthiede/prometheus-remote/releases/download/prometheus-remote-0.1.1/prometheus-remote-0.1.1.tgz -n prom --create-namespace
```
