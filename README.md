# Firefox

[![AlmaLinux9-CI](https://github.com/philnewm/ansible-firefox/actions/workflows/almalinux9-ci-caller.yml/badge.svg)](https://github.com/philnewm/ansible-firefox/actions/workflows/almalinux9-ci-caller.yml) [![Rocky9-CI](https://github.com/philnewm/ansible-firefox/actions/workflows/rocky9-ci-caller.yml/badge.svg)](https://github.com/philnewm/ansible-firefox/actions/workflows/rocky9-ci-caller.yml) [![CentOSStream9-CI](https://github.com/philnewm/ansible-firefox/actions/workflows/centosstream9-ci-caller.yml/badge.svg)](https://github.com/philnewm/ansible-firefox/actions/workflows/centosstream9-ci-caller.yml) [![Fedora43-CI](https://github.com/philnewm/ansible-firefox/actions/workflows/fedora43-ci-caller.yml/badge.svg)](https://github.com/philnewm/ansible-firefox/actions/workflows/fedora43-ci-caller.yml)<br>
[![Ubuntu2404-CI](https://github.com/philnewm/ansible-firefox/actions/workflows/ubuntu2404-ci-caller.yml/badge.svg)](https://github.com/philnewm/ansible-firefox/actions/workflows/ubuntu2404-ci-caller.yml) [![Debian13-CI](https://github.com/philnewm/ansible-firefox/actions/workflows/debian13-ci-caller.yml/badge.svg)](https://github.com/philnewm/ansible-firefox/actions/workflows/debian13-ci-caller.yml)

Role description

This role includes a molecule testing setup at `molecule`

## Structure

```code
📦 ansible-firefox
 ┣ 📂 defaults
 ┃ ┗ 📜 main.yml
 ┣ 📂 meta
 ┃ ┗ 📜 main.yml
 ┣ 📂 molecule
 ┃ ┗ 📂 default
 ┃   ┗ 📜, 📜, 📜, scenario_files
 ┣ 📂tasks
 ┃ ┣ 📜absent.yml
 ┃ ┣ 📜default.yml
 ┃ ┣ 📜esr.yml
 ┃ ┣ 📜extensions.yml
 ┃ ┣ 📜flatpak.yml
 ┃ ┣ 📜main.yml
 ┃ ┣ 📜present.yml
 ┃ ┣ 📜purge_snap.yml
 ┃ ┣ 📜setup_mozilla_repo_debian.yml
 ┃ ┗ 📜tests.yml
 ┣ 📂 vars
 ┃ ┗ 📜 main.yml
 ┗ 🗒️ README.md

```

Describe and explain role structure.

## Requirements

Elaborate external dependencies and how to use them.

## Role Variables

* defaults/main.yml
  * first_var
  * sec_var
  * third_var
* vars/main.yml
  * first_var
  * sec_var
  * third_var

## Dependencies

List role ansible-galaxy dependencies - if any.

## Example Playbook

Add an example playbook

```yaml
---

tasks:
  - name: Include ansible-firefox present
    ansible.builtin.include_role:
      name: ansible-firefox
    vars:
      state: present
      firefox_source: default
      firefox_extensions_enabled: true
...
```

## License

Add license - if any.

## Changes to role template

* Add github action that flags empty directories on release creation

## Git submodule molecule

`git submodule add <url-of-shared-molecule-repo> molecule`

`.git/info/attributes`

```code
molecule/default/cleanup.yml merge=ours
molecule/default/converge.yml merge=ours
molecule/default/verify.yml merge=ours
```

```bash
git submodule update --remote --merge
```

```bash
cd molecule
git pull origin main
```
