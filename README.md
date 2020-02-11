# joscherrer.tmux

[![Build Status](https://travis-ci.com/joscherrer/tmux.svg?branch=master)](https://travis-ci.com/joscherrer/tmux)
[![Galaxy](https://img.shields.io/badge/galaxy-joscherrer.tmux-blue.svg)](https://galaxy.ansible.com/joscherrer/tmux/)

Role to install tmux

## Requirements

None.

## Role Variables

### Default usage

As default tmux is installed and running.
If you want to adapt this to your needs look at the [Advanced usage](#advanced-usage) section.

### Advanced usage

For more advanced usage the following variables are available:
```yaml
tmux_source_path: "{{ global_source_path | default('/opt') }}"
tmux_prefix: "{{ global_prefix | default('/usr/local') }}"
tmux_user_install: "{{ global_user_install | default(false) }}"
tmux_user_config: "{{_global_user_config | default(false) }}"
tmux_skel_config: "{{ global_skel_config | default(false) }}"
tmux_install_from_source: "{{ global_install_from_source | default(false) }}"
tmux_source_url: "https://github.com/user/tmux/archive/tmux-{{ tmux_git_version }}.tar.gz"
tmux_force_install: "{{ global_force_install | default(false) }}"
tmux_user_strip: "{{ global_user_strip | default([]) }}"
tmux_user_filter: "{{ global_user_filter | default([])}}"
tmux_version: ""
```

## Dependencies

None

## Example Playbook

Install tmux with the default settings
```yaml
- hosts: all
  roles:
     - role: joscherrer.tmux
```

## License

BSD-3-Clause-Clear

## Author Information

This role was created in 2020 by [Jonathan Scherrer].
