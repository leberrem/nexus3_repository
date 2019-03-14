Role Name
=========

Install and configure NEXUS.

Requirements
------------

docker daemon on host.

Role Variables
--------------

```yaml
    nexus_data: "/var/nexus/data"
    nexus_plugin: "/var/nexus/plugins"
    container_name: "nexus"
    docker_image: sonatype/nexus3:lastest
    install_helm_plugin: true
    install_nexus: true
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
        nexus_data: "/var/nexus/data"
        nexus_plugin: "/var/nexus/plugins"
        container_name: "nexus"
        docker_image: sonatype/nexus3:lastest
        install_helm_plugin: true
        install_nexus: true

```

License
-------

...

Author Information
------------------

WeScale
