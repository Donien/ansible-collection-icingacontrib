# Ansible Collection - netways.icinga_contrib

This Collection is meant to be an addition to the official [Ansible Collection by Icinga](https://github.com/Icinga/ansible-collection-icinga/).  
Since Icinga's Collection currently only handles official Icinga components, **netways.icinga_contrib** aims to fill the gap.

For example, there are Icinga Web 2 modules provided by the community which are used a lot like the [Grafana module](https://github.com/Mikesch-mp/icingaweb2-module-grafana) or the [Map module](https://github.com/nbuchwitz/icingaweb2-module-map).  
This Collection is meant to handle such cases.

## Installing the Collection

**Ansible Galaxy**  
To install the Collection from Ansible Galaxy:

```
ansible-galaxy collection install netways.icinga_contrib
```

**Git**  
To install the Collection's main branch from this repository:

```
ansible-galaxy collection install git+https://github.com/netways/ansible-collection-icinga_contrib,main
```

To install a specific tag release:

```
ansible-galaxy collection install git+https://github.com/netways/ansible-collection-icinga_contrib,1.2.3
```

## Using the Collection

To use the collection specify the FQCN of the module, plugin or role you want to use.

```yaml
- name: Run role netways.icinga_contrib.icingaweb2_modules
  hosts: somehost

  vars:
    icingaweb2_modules:
      grafana:
        ...

  roles:
    - netways.icinga_contrib.icingaweb2_modules
```

## Roles

- **[netways.icinga_contrib.icingaweb2_modules](./roles/icingaweb2_modules/README.md)**  
  This role is used to manage modules for Icinga Web 2 not managed by Icinga's official Collection.

## License

GPL-3.0-only
