# Example Ansible Playbook for Deception Logic

## Configuration

site.yml:

```yaml
---
- hosts:
  - server01
  - server02
  vars:
    - key_id: '665afd50-1c58-11e9-ab14-d663bd87'
    - secret_key: 'ece926d8c0356205276a45266d361161'
    - log_file_retention:'30'
  roles:
    - ansible_deception-agent
```

/etc/ansible/hosts:

```yaml
server01
server02
# if python not available on server use python3
server03 testxenial ansible_python_interpreter=/usr/bin/python3
```

## Deploying

run:

```shell
anisble-playbook site.yml
```

tested on centos6 centos7 , debian jessie and stretch , ubuntu xenial trusty and artful