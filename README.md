Role Name
=========

Install and configure NEXUS.

Requirements
------------

docker daemon on host.

Role Variables
--------------

```yaml
    nexus3_repository_data_directory: "/var/nexus/data"
    nexus3_repository_plugin_directory: "/var/nexus/plugins"
    nexus3_repository_container_name: "nexus"
    nexus3_repository_container_image: "sonatype/nexus3:latest"
    nexus3_repository_install_helm_plugin: true
    nexus3_repository_install_nexus: true
```

Dependencies
------------

No dependencies.

Example Playbook
----------------

```yaml
- hosts: servers
  become : yes
  tasks:
    - name: install and configure nexus
      include_role:
        name: nexus3_repository
      vars:
        nexus3_repository_data_directory: "/var/nexus/data"
        nexus3_repository_plugin_directory: "/var/nexus/plugins"
        nexus3_repository_container_name: "nexus"
        nexus3_repository_container_image: "sonatype/nexus3:latest"
        nexus3_repository_install_helm_plugin: true
        nexus3_repository_install_nexus: true

```

License
-------

GPLv3

Author Information
------------------

Mikaël LE BERRE
