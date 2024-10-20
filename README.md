# Role Name

https://gist.github.com/aaronlippold/d1183270274568159d6a7b098441ec4c
https://braheezy.github.io/posts/automating-firefox-with-ansible/
https://askubuntu.com/questions/73474/how-to-install-firefox-addon-from-command-line-in-scripts
https://wiki.mozilla.org/Firefox/CommandLineOptions#Using_command_line_options
https://linuxconfig.org/how-to-customize-firefox-using-the-policies-json-file

[![ci-testing](https://github.com/philnewm/ansible-firefox/actions/workflows/molecule-ci.yml/badge.svg)](https://github.com/philnewm/ansible-firefox/actions/workflows/molecule-ci.yml)

Role description

This role includes a full vagrant based molecule testing setup at `extensions/molecule/default`

## Structure

```code
📦 ansible-firefox
 ┣ 📂 defaults
 ┃ ┗ 📜 main.yml
 ┣ 📂 files
 ┃ ┗ 📜 file_placeholder.yml
 ┣ 📂 handlers
 ┃ ┗ 📜 main.yml
 ┣ 📂 meta
 ┃ ┗ 📜 main.yml
 ┣ 📂 molecule
 ┃ ┗ 📂 default
 ┃   ┗ 📜, 📜, 📜, scenario_files
 ┣ 📂 tasks
 ┃ ┣ 📜 main.yml
 ┃ ┣ 📜 present.yml
 ┃ ┣ 📜 dependencies.yml
 ┃ ┣ 📜 absent.yml
 ┃ ┗ 📜 init.yml
 ┣ 📂 templates
 ┃ ┗ ⛩️ template.j2
 ┣ 📂 vars
 ┃ ┗ 📜 main.yml
 ┗ 🗒️ README.md
 ┗ 📓 requirements.txt

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
      firefox_state: present

...
```

## License

Add license - if any.

## Changes to role template

* Add github action that flags empty directories on release creation
