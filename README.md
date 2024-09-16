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
