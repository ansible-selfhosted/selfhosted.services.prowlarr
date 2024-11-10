[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Copier](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/copier-org/copier/master/img/badge/badge-grayscale-inverted-border.json)](https://github.com/copier-org/copier)
[![Podman Badge](https://img.shields.io/badge/Podman-892CA0?logo=podman&logoColor=white)](https://podman.io/)
[![Hatch project](https://img.shields.io/badge/%F0%9F%A5%9A-Hatch-4051b5.svg)](https://github.com/pypa/hatch)
![CI](https://github.com/ansible-selfhosted/selfhosted.services.prowlarr/actions/workflows/ci.yml/badge.svg)
[![Ansible](https://img.shields.io/badge/Ansible-Molecule-EE0000?style=plastic&logo=ansible&logoColor=white)](https://github.com/ansible/molecule)

<!-- BEGIN_ANSIBLE_DOCS -->

# Ansible Role: [prowlarr](https://wiki.servarr.com/en/prowlarr)

A role to deploy Prowlarr using rootless Podman with systemd

## Role Requirements

- none

*Refer to services collection for general requirements*

## Role Arguments

|Option|Description|Type|Required|Default|choices|
|---|---|---|---|---|---|
|prowlarr_config_path|The path to the prowlarr configuration directory|str|False|~/.config/prowlarr/|
|prowlarr_data_path|The path to the prowlarr data directory<br>It is recommended to share the same data directory with other media managing services|str|False|~/.local/share/containers/storage/media|
|prowlarr_timezone|The timezone for the prowlarr service|str|False|Etc/UTC|
|prowlarr_version|The version of prowlarr to install|str|False|latest|- latest<br>- develop<br>- nightly
|prowlarr_web_port|The port for the web server|int|False|9696|


## Example Playbook

```
- hosts: all
  tasks:
    - name: Importing prowlarr role
      ansible.builtin.import_role:
        name: selfhosted.services.prowlarr
      vars:
```

## License

This project is licensed under the [MIT License](LICENSE)


⊂(▀¯▀⊂)

<!-- END_ANSIBLE_DOCS -->
