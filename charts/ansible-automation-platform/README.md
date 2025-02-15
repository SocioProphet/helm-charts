# Ansible Automation Platform Operator Helm Deploy

Ansible Automation Platform Helm Chart customises and deploys the [Ansible Automation Platform](https://www.ansible.com/products/automation-platform) project using the [Operator](https://catalog.redhat.com/software/containers/ansible-automation-platform/platform-resource-operator-bundle/5f6a0f6bff00777e832818ac) written by Red Hat.

## Installing the chart

To install the chart from source:

```bash
helm upgrade --install ansible-automation-platform -f values.yaml . --create-namespace --namespace ansible-automation-platform
```

The above command creates objects with default naming convention and configuration.

## Removing

To delete the chart:

```bash
helm uninstall ansible-automation-platform --namespace ansible-automation-platform
```

## Troubleshooting

If your chart only partially installed you can try disabling hooks when deleting

```bash
helm delete ansible-automation-platform --no-hooks
```

## Configuration

The [values.yml](values.yaml) file contains instructions for common chart overrides.
