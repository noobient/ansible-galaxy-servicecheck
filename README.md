# noobient.servicecheck

## Synopsys

This role checks the state of systemd units.

## Parameters

| Name | Required | Example | Description |
|---|---|---|---|
| `unit` | yes | `firewalld.service` | Name of the systemd unit to check. |

## Examples

```yml
- include_role:
    name: noobient.servicecheck
  vars:
    unit: 'firewalld.service'
```

## Return Values

| Key | Type | Example | Description |
|---|---|---|---|
| `servicecheck.systemd` | boolean | `true` | Indicates whether the host was booted with systemd. If not, all other values will be false as well. |
| `servicecheck.exists` | boolean | `true` | Indicates whether the given systemd unit exists on the host. |
| `servicecheck.started` | boolean | `false` | Indicates whether the given system unit is running. |

## Support

| Platform | Support | Status |
|---|---|---|
| Linter | ✅ | [![Lint](https://github.com/noobient/ansible-galaxy-servicecheck/actions/workflows/lint.yml/badge.svg)](https://github.com/noobient/ansible-galaxy-servicecheck/actions/workflows/lint.yml) |
| AlmaLinux 8 | ✅ | [![AlmaLinux 8](https://github.com/noobient/ansible-galaxy-servicecheck/actions/workflows/almalinux-8.yml/badge.svg)](https://github.com/noobient/ansible-galaxy-servicecheck/actions/workflows/almalinux-8.yml) |
| AlmaLinux 9 | ✅ | [![AlmaLinux 9](https://github.com/noobient/ansible-galaxy-servicecheck/actions/workflows/almalinux-9.yml/badge.svg)](https://github.com/noobient/ansible-galaxy-servicecheck/actions/workflows/almalinux-9.yml) |
| Fedora 40 | ✅ | [![Fedora 40](https://github.com/noobient/ansible-galaxy-servicecheck/actions/workflows/fedora-40.yml/badge.svg)](https://github.com/noobient/ansible-galaxy-servicecheck/actions/workflows/fedora-40.yml) |
| Fedora 41 | ✅ | [![Fedora 41](https://github.com/noobient/ansible-galaxy-servicecheck/actions/workflows/fedora-41.yml/badge.svg)](https://github.com/noobient/ansible-galaxy-servicecheck/actions/workflows/fedora-41.yml) |
| Ubuntu 20.04 | ✅ | [![Ubuntu 20.04](https://github.com/noobient/ansible-galaxy-servicecheck/actions/workflows/ubuntu-20.04.yml/badge.svg)](https://github.com/noobient/ansible-galaxy-servicecheck/actions/workflows/ubuntu-20.04.yml) |
| Ubuntu 22.04 | ✅ | [![Ubuntu 22.04](https://github.com/noobient/ansible-galaxy-servicecheck/actions/workflows/ubuntu-22.04.yml/badge.svg)](https://github.com/noobient/ansible-galaxy-servicecheck/actions/workflows/ubuntu-22.04.yml) |
| Ubuntu 24.04 | ✅ | [![Ubuntu 24.04](https://github.com/noobient/ansible-galaxy-servicecheck/actions/workflows/ubuntu-24.04.yml/badge.svg)](https://github.com/noobient/ansible-galaxy-servicecheck/actions/workflows/ubuntu-24.04.yml) |
