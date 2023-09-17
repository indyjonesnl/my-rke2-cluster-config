RKE2 uses a default configuration file at path `/etc/rancher/rke2/config.yaml`.
I added the following configuration:
```
node-external-ip: "96.96.96.96"
tls-san:
  - "96.96.96.96"
  - "domain.com"
```
This configures the cluster to generate a certificate that can be used on both the internal IP address and the external IP address, allowing external access for kubectl (or Lens).
