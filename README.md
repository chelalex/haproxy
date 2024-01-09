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

haproxy:<br>
&nbsp; ssl_path: *path to ssl certs*<br>
&nbsp; key: *keyfile name*<br>
&nbsp; cert: *certfile name*<br>
&nbsp; ssl_file: *total file (key + cert)*<br>
&nbsp; config_path: *path to config file*<br>
&nbsp; config_file: *config file name*<br>
config_params: *config parameters*<br>
&nbsp; \- section: *parameters section*<br>
&nbsp; section_name: *given section name*<br>
&nbsp; options: *options array*<br>
&nbsp; &nbsp; \- name: *option name*<br>
&nbsp; &nbsp; &nbsp; value: *option value*<br>
&nbsp; &nbsp; ...<br>
&nbsp; ...<br>
&nbsp; *(all options are described in HAproxy documentation)*<br>

## Example Playbook

    - hosts: proxy_server
      roles:
         - haproxy