# application

![Version: 1.2.0](https://img.shields.io/badge/Version-1.2.0-informational?style=flat-square)  ![AppVersion: 1.0.0](https://img.shields.io/badge/AppVersion-1.0.0-informational?style=flat-square)

## Description

A Helm chart for Kubernetes

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| daidv94 | <dai.dao@galaxyfinx.com> |  |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| autoscaling.enabled | bool | `false` |  |
| autoscaling.maxReplicas | int | `100` |  |
| autoscaling.minReplicas | int | `1` |  |
| autoscaling.targetCPUUtilizationPercentage | int | `80` |  |
| configMaps | list | `[]` |  |
| deployment.affinity | object | `{}` |  |
| deployment.annotations | object | `{}` |  |
| deployment.arguments | object | `{}` |  |
| deployment.configmapExtra | string | `""` |  |
| deployment.dnsConfig | list | `[]` |  |
| deployment.env | object | `{}` |  |
| deployment.extraEnvs | list | `[]` |  |
| deployment.extraInitContainers | list | `[]` |  |
| deployment.initContainer | object | `{}` |  |
| deployment.livenessProbe | object | `{}` |  |
| deployment.nodeSelector | object | `{}` |  |
| deployment.podAnnotations | object | `{}` |  |
| deployment.podSecurityContext | object | `{}` |  |
| deployment.ports[0].containerPort | int | `8080` |  |
| deployment.ports[0].name | string | `"http"` |  |
| deployment.ports[0].protocol | string | `"TCP"` |  |
| deployment.ports[1].containerPort | int | `8081` |  |
| deployment.ports[1].name | string | `"management"` |  |
| deployment.ports[1].protocol | string | `"TCP"` |  |
| deployment.readinessProbe | object | `{}` |  |
| deployment.resources.limits.cpu | string | `"500m"` |  |
| deployment.resources.limits.memory | string | `"1024Mi"` |  |
| deployment.resources.requests.cpu | string | `"250m"` |  |
| deployment.resources.requests.memory | string | `"512Mi"` |  |
| deployment.revisionHistoryLimit | int | `3` |  |
| deployment.securityContext | object | `{}` |  |
| deployment.startupProbe | object | `{}` |  |
| deployment.strategy | object | `{}` |  |
| deployment.terminationGracePeriodSeconds | int | `60` |  |
| deployment.tolerations | list | `[]` |  |
| deployment.volumeMounts | list | `[]` |  |
| deployment.volumes | list | `[]` |  |
| global.env | object | `{}` |  |
| global.extraLabels | list | `[]` |  |
| global.fullnameOverride | string | `""` |  |
| global.image.pullPolicy | string | `"Always"` |  |
| global.image.repository | string | `""` |  |
| global.image.tag | string | `""` |  |
| global.imagePullSecrets | list | `[]` |  |
| global.nameOverride | string | `""` |  |
| global.releaseVersion | string | `""` |  |
| ingress.annotations | object | `{}` |  |
| ingress.className | string | `""` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts[0].host | string | `"chart-example.local"` |  |
| ingress.hosts[0].paths[0].path | string | `"/"` |  |
| ingress.hosts[0].paths[0].pathType | string | `"ImplementationSpecific"` |  |
| ingress.tls | list | `[]` |  |
| kedaAutoscaling.cooldownPeriod | int | `300` |  |
| kedaAutoscaling.enabled | bool | `false` |  |
| kedaAutoscaling.extraTriggers | list | `[]` |  |
| kedaAutoscaling.maxReplicas | int | `10` |  |
| kedaAutoscaling.minReplicas | int | `1` |  |
| pvc.accessMode | string | `"ReadWriteOnce"` |  |
| pvc.annotations | object | `{}` |  |
| pvc.enabled | bool | `false` |  |
| pvc.path | string | `"/mount"` |  |
| pvc.size | string | `"1Gi"` |  |
| pvc.storageClass | string | `"default"` |  |
| rbac.create | bool | `true` |  |
| replicaCount | int | `1` |  |
| secret | object | `{}` |  |
| service.additionalPorts | list | `[]` |  |
| service.nameOverride | string | `""` |  |
| service.port | int | `8080` |  |
| service.protocol | string | `"TCP"` |  |
| service.targetPort | string | `"http"` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `""` |  |
| virtualService.allowedHosts[0] | string | `"*"` |  |
| virtualService.enabled | bool | `true` |  |
| virtualService.gateways[0] | string | `"gateway"` |  |
| virtualService.http.destinationPort | int | `8080` |  |
| virtualService.http.prefixURI[0] | string | `"/foo"` |  |
| virtualService.http.timeout | string | `"1m"` |  |
