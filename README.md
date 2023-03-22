
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
### Example
```yaml
potos_wallpaper_images:
  - name: "Potos"
    filename: "potos.jpg"
    options: "zoom"
    pcolor: "#161b21"
    scolor: "#161b21"
    shade_type: "solid"
```
| variable   | Possible values                                                           | Description                                                             |
|------------|---------------------------------------------------------------------------|-------------------------------------------------------------------------|
| name       |                                                                           | How the wallpaper is named to the user                                  |
| filename   |                                                                           |                                                                         |
| options    | "none", "wallpaper", "centered", "scaled", "stretched", "zoom", "spanned" | Determines how the image is rendered                                    |
| pcolor     | any hex rgb value e.g. #161b21                                            | Left or top color when drawing gradients, or the solid color.           |
| scolor     | any hex rgb value e.g. #161b21                                            | Right or bottom color when drawing gradients, not used for solid color. |
| shade_type | "horizontal", "vertical", and "solid"                                     | How to shade the background color.                                      |

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

