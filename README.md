# Ansible role: PACMAN

This role install and manage:
 - pacman
 - pacman hooks
 - custom arch repositories
 - paru (AUR helper)
 - reflector
 - system upgrade

## Usage
Override [defaults](https://github.com/lunics/ansible_role_pacman/blob/main/defaults/main.yml)
```yaml
aur_helper: paru
aur_user:   aur
upgrade:    true

arch_repo:
  - name:     custom-repo
    server:   http://domain-arch-repo:80/
    siglevel: Required DatabaseOptional
    key:
      path:   "{{ path_play }}/files/keys/custom-repo.gpg"
      hash:   F17ABE74A88A1101
```
TODO
- add pacman hooks feature
- manage aur with and without aur_user
