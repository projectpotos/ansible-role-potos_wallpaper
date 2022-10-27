
# Ansible Role - potos\_wallpaper

Role to manage wallpapers of Potos Linux Clients.

[![Test](https://github.com/projectpotos/ansible-role-potos_wallpaper/actions/workflows/test.yml/badge.svg)](https://github.com/projectpotos/ansible-role-potos_wallpaper/actions/workflows/test.yml)

## Example Playbook

As this role is tested via Molecule one can use [that
playbook](./molecule/default/converge.yml) as a starting point:

```yaml
---

- name: Converge
  hosts: all
  gather_facts: yes
  tasks:
    - name: run role
      ansible.builtin.include_role:
        name: 'ansible-role-potos_wallpaper'
```

## Role Variables

The default variables are defined in [defaults/main.yml](./defaults/main.yml):

```yaml
# List of files to be found under `potos_wallpaper` to be added as background,
# first element is set as default
potos_wallpaper_images: []
```

Another option is to use `ansible-doc` to read the argument specification:

```sh
ansible-doc --type role -r . main ansible-role-potos_wallpaper
```

## Requirements

Files listed under `potos_wallpaper_images` need to exist under
`potos_wallpaper/`.

## License

See [LICENSE](./LICENSE)

## Author Information

[Project Potos](https://github.com/projectpotos)

