# k8s-yaml
```
## metalLB configmap
echo '
apiVersion: v1
kind: ConfigMap
metadata:
  namespace: metallb-system
  name: config
data:
  config: |
    address-pools:
    - name: mlb1
      protocol: layer2
      addresses:
      - 192.168.135.220-192.168.135.230' | kubectl apply -f -
```
