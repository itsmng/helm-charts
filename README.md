
![](https://static.wixstatic.com/media/e5b7d4_f67ff8c629844818a6e3e43550cb1e17~mv2.png/v1/fill/w_348,h_122,al_c,q_85,usm_0.66_1.00_0.01,enc_auto/Original%20on%20Transparent.png)

ITSM-NG is a GLPI fork with the objective of offering a strong community component and relevant technological choices.

# Some Links

  - [Website](https://www.itsm-ng.com)
  - [Github](https://github.com/itsmng)
  - [Wiki](https://wiki.itsm-ng.org)

## Get the Chart

### Add Helm repository

```bash
helm repo add itsmng https://chart.itsm-ng.org
helm repo update
```

### Retrieve the values.yaml 

```bash
wget https://raw.githubusercontent.com/itsmng/helm-charts/master/values.yaml
```

### Installing the Chart

```bash
helm -n <namespace> install <release_name> itsmng/itsm-ng -f ./values.yaml --create-namespace
```

### Upgrading the Chart

```bash
helm -n <namespace> upgrade <release_name> itsmng/itsm-ng -f ./values.yaml
```

### Uninstalling the Chart

```bash
helm uninstall -n <namespace> <release_name>
kubectl delete ns <namespace>
```
