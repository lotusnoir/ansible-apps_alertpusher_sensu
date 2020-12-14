# Ansible Role: ansible-apps_alertpusher

## Description

[![Build Status](https://travis-ci.com/lotusnoir/ansible-apps_alertpusher.svg?branch=master?style=flat)](https://travis-ci.com/lotusnoir/ansible-apps_alertpusher)
[![License](https://img.shields.io/badge/license-Apache--2.0-brightgreen?style=flat)](https://opensource.org/licenses/Apache-2.0)
[![Ansible Role](https://img.shields.io/badge/galaxy-apps_alertpusher-purple?style=flat)](https://galaxy.ansible.com/lotusnoir/apps_alertpusher)
![GitHub repo size](https://img.shields.io/github/repo-size/lotusnoir/ansible-apps_alertpusher?color=orange&style=flat)
![Ansible Quality Score](https://img.shields.io/ansible/quality/52300)
[![downloads](https://img.shields.io/ansible/role/d/52300)](https://galaxy.ansible.com/lotusnoir/apps_alertpusher)
[![Version](https://img.shields.io/github/release/lotusnoir/ansible-apps_alertpusher.svg)](https://github.com/lotusnoir/ansible-apps_alertpusher/releases/)
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_alertpusher&metric=alert_status)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_alertpusher)
[![Maintainability Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_alertpusher&metric=sqale_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_alertpusher)
[![Reliability Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_alertpusher&metric=reliability_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_alertpusher)
[![Security Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_alertpusher&metric=security_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_alertpusher)

Deploy [alertpusher](https://github.com/lotusnoir/alertmanager-apps_alertpusher_sensu) to send prometheus alerts to sensu uchiwa.

## Role variables

| Name                            | Default Value    | Description                        |
| ------------------------------- | ---------------- | -----------------------------------|
| `alertpusher_install_dir`       | /usr/local/bin   | directory to install binary |
| `alertpusher_force_install`     | false            | force install variable |
| `alertpusher_src_dir`           | /tmp/alertpusher | temp dir to build sources |
| `alertpusher_debug`             |  | |
| `alertpusher_sensu_client_port` |  | |
| `alertpusher_sensu_api_port`    |  | |
| `alertpusher_targets`           |  | |

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
