# Ansible gnu_linux role

This is an [Ansible](http://www.ansible.com) wrapper role which configures any standard GNU/Linux using the following dependant roles:

- environment

See dependant roles documentation to know how to configure each one.

## Dependencies

- Ansible >= 2.0
- Role environment.

## Variables

A list of all the default variables for this role is available in `defaults/main.yml`.

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

Not defined.

## Author Information

- Juan Antonio Valiño García ([juanval@edu.xunta.es](mailto:juanval@edu.xunta.es)). Amtega - Xunta de Galicia
