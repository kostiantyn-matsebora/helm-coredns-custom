# Core DNS custom configuration

Helm chart provides custom configuration for CoreDNS.

More information about the feature itself can be found here https://learn.microsoft.com/en-us/azure/aks/coredns-custom

For now, it supports only adding hosts.

## Configuration

Example:

```yaml
    - hosts: 
        - name: longhorn.local # host name
            ip: 192.168.2.100 # IP address
        - name: dashboard.local
            ip: 192.168.2.100
        - name: vault.local
            ip: 192.168.2.100
```

## Usage

Add helm [repository](https://kostiantyn-matsebora.github.io/helm-charts/) first:

```bash
helm repo add kostiantyn-matsebora https://kostiantyn-matsebora.github.io/helm-charts/
```

Install/upgrade helm chart using your custom values:

```bash

helm upgrade oauth2-proxy kostiantyn-matsebora/helm-coredns-custom --install --values ./custom-values.yaml

```

## Contributing

If you experience any issues, have a question or a suggestion, or if you wish
to contribute, feel free to [open an issue][issues] or
[start a discussion][discussions].

[issues]: https://github.com/kostiantyn-matsebora/helm-coredns-custom/issues
[discussions]: https://github.com/kostiantyn-matsebora/helm-coredns-custom/discussions

## License

[`MIT License`](../LICENSE)
