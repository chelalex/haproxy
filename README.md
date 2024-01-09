# haproxy

Install and configure HAproxy ansible role
Available for Ubuntu 22.04 LTS

    haproxy
    ├── README.md
    ├── tasks
    │   └── main.yml
    ├── templates
    │   └── haproxy.cfg.j2
    └── vars
        └── main.yml

## Requirements

openssl

## Role Variables

haproxy:
  ssl_path: *path to ssl certs*<br>
  key: *keyfile name*<br>
  cert: *certfile name*<br>
  ssl_file: *total file (key + cert)*<br>
  config_path: *path to config file*<br>
  config_file: *config file name*<br>
config_params: *config parameters*<br>
  \- section: *parameters section*<br>
    section_name: *given section name*<br>
    options: *options array*<br>
      \- name: *option name*<br>
        value: *option value*<br>
        ...<br>
    ...<br>
    *(all options are described in HAproxy documentation)*<br>

## Example Playbook

    - hosts: proxy_server
      roles:
         - haproxy