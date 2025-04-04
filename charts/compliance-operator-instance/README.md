# compliance-operator-instance

![Version: 0.1.0](https://img.shields.io/badge/Version-0.1.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.16.0](https://img.shields.io/badge/AppVersion-1.16.0-informational?style=flat-square)

A Helm chart for Kubernetes

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| customScanSetting | object | `{"debug":false,"enabled":false,"name":"moderate","roles":["worker","master"],"schedule":"0 1 * * *","tolerations":[{"effect":"Noschedule","key":"node-role.kubernetes.io/master","oprerator":"exist"}]}` | Define a custom scan setting |
| profiles | list | `[{"apiGroup":"compliance.openshift.io/v1alpha1","kind":"Profile","name":"ocp4-cis-node"},{"apiGroup":"compliance.openshift.io/v1alpha1","kind":"Profile","name":"ocp4-cis"}]` | Select the Compliance Profiles to run |
| settingName | string | `"default"` | The ScanSetting to use |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.14.2](https://github.com/norwoodj/helm-docs/releases/v1.14.2)
