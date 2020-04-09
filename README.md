[![Build Status](https://travis-ci.org/open-io/ansible-role-openio-monitoring.svg?branch=master)](https://travis-ci.org/open-io/ansible-role-openio-monitoring)
# Ansible role `monitoring`

An Ansible role for install monitoring. Specifically, the responsibilities of this role are to:

- install and configure the full OpenIO monitoring stack

## Requirements

- Ansible 2.9+

## Role usage
This is not a real ansible role but it holds a playbook (in `playbooks/main.yml`)
that is called from the customer-skeleton. There is no tasks or variables.

There are some dependancies defined in `meta/main.yml` in order to pull specific
roles when requirements are installed (through `ansible-galaxy`).

## Dependencies
- https://github.com/open-io/ansible-role-openio-service
- see `meta/main.yml` for more dependancies

## Example Playbook

```yaml
- hosts: all
  gather_facts: true
  become: true

  tasks:
    - name: Monitoring
      import_playbook: roles/monitoring/playbooks/main.yml

```

## Contributing

Issues, feature requests, ideas are appreciated and can be posted in the Issues section.

Pull requests are also very welcome.
The best way to submit a PR is by first creating a fork of this Github project, then creating a topic branch for the suggested change and pushing that branch to your own fork.
Github can then easily create a PR based on that branch.

## License
Copyright (C) 2015-2020 OpenIO SAS
