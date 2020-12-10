# Ansible Role: ansible-apps_alertpusher

## Description

[![Build Status](https://travis-ci.com/lotusnoir/ansible-apps_alertpusher.svg?branch=master)](https://travis-ci.com/lotusnoir/ansible-apps_alertpusher)[![License](https://img.shields.io/badge/license-Apache--2.0-brightgreen)](https://opensource.org/licenses/Apache-2.0)[![Ansible Role](https://img.shields.io/badge/ansible%20role-apps__alertpusher-blue)](https://galaxy.ansible.com/lotusnoir/ansible-apps_alertpusher/)[![GitHub tag](https://img.shields.io/badge/version-latest-blue)](https://github.com/lotusnoir/ansible-apps_alertpusher/tags)

Deploy [alertpusher](https://github.com/lotusnoir/alertmanager-apps_alertpusher_sensu) to send prometheus alerts to sensu uchiwa.

## Role variables

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `alertpusher_install_dir` | /usr/local/bin | directory to install binary |
| `alertpusher_force_install` | false | force install variable |
| `alertpusher_src_dir` | /tmp/alertpusher | temp dir to build sources |
| `alertpusher_debug` |  | |
| `alertpusher_sensu_client_port` |  | |
| `alertpusher_sensu_api_port` |  | |
| `alertpusher_targets` |  | |

## Examples

	---
	- hosts: apps_alertpusher
	  become: yes
	  become_method: sudo
	  gather_facts: yes
	  roles:
	    - role: ansible-apps_alertpusher
	  environment: 
	    http_proxy: "{{ http_proxy }}"
	    https_proxy: "{{ https_proxy }}"
	    no_proxy: "{{ no_proxy }}

## License

This project is licensed under Apache License. See [LICENSE](/LICENSE) for more details.
