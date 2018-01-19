# Ansible gnu_linux role

This is an [Ansible](http://www.ansible.com) wrapper role which configures a standard GNU/Linux another dependant roles.

See dependant roles documentation to know how to configure each one.

## Requirements

- Ansible >= 2.4

## Variables

A list of all the default variables for this role is available in `defaults/main.yml`.

## Dependencies

- amtega.environment (if internet proxy is used).

## Usage

This is an example playbook:

```yaml
---

- hosts: all
  roles:
    - gnu_linux
```

## Testing

Test are based on docker containers. You can run the tests with the following commands:

```shell
$ cd gnu_linux/test
$ ansible-playbook main.yml
```

If you have docker engine configured you can avoid running dependant 'docker_engine' role (that usually requries root privileges) with the following commands:

```shell
$ cd gnu_linux/test
$ ansible-playbook --skip-tags "role::docker_engine" main.yml
```

## License

Copyright (C) 2017 AMTEGA - Xunta de Galicia

This role is free software: you can redistribute it and/or modify
it under the terms of:
GNU General Public License version 3, or (at your option) any later version;
or the European Union Public License, either Version 1.2 or – as soon
they will be approved by the European Commission ­subsequent versions of
the EUPL;

This role is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details or European Union Public License for more details.

## Author Information

- Juan Antonio Valiño García
