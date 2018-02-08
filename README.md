# ssm-seelog-config

Configure seelog

## Requirements

ssm agent is installed

## Role Variables
- ssm_agent_configuration_dir: datadog checks config directory.
  This default to `/etc/amazon/ssm/`
- log_group_name: ssm agent configuration in xml that will be dropped into `{{ ssm_agent_configuration_dir }}`

## Dependencies

## Example Playbook

```
---
- hosts: all
  become: True
  roles:
    - name: ssm-seelog-config
      ssm_agent_configuration_dir: "/etc/amazon/ssm/"
      log_group_name: "error.log"
```

## License

MIT

## Author Information

[Igit Soeriasaputra](https://github.com/radengoots)
