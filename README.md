# Ansible Role Terraform

Library of Ansible plugins and roles for deploying various services.
See [ansible-roles](https://github.com/davidfischer-ch/ansible-roles) for additional documentation.

This repository hosts the role terraform and may depend of other roles and plugins of the library.

## Dependencies

See [meta](meta/main.yml).

## Variables

TODO VARIABLES

## Example

### Playbook

```
---

- hosts: localhost
  roles:
    - terraform
  vars:
    go_version: 1.14.2
    go_release_checksum: sha256:6272d6e940ecb71ea5636ddb5fab3933e087c1356173c61f4a803895e947ebb3

    terraform_version: 0.12.23
    terraform_release_checksum: sha256:78fd53c0fffd657ee0ab5decac604b0dea2e6c0d4199a9f27db53f081d831a45

    terraform_providers:
      - name: AWX
        url: https://github.com/davidfischer-ch/terraform-provider-awx.git
        path: github.com/davidfischer-ch/terraform-provider-awx
        version: v0.2.3
        environment:
          BINARY: /usr/local/bin/terraform-provider-awx
```

## License

See [LICENSE.rst](LICENSE.rst).

## Authors

See [AUTHORS](AUTHORS).

2014-2020 - David Fischer
