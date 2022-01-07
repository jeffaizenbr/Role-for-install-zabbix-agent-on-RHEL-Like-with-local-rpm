# Role-for-install-zabbix-agent-on-RHEL-Like-with-local-rpm


##Example Playbook /etc/ansible/zabbix-agent.yml
```bash
---
- hosts: zabbix-clients
  roles:
    - role: zabbix-agent
      vars:
        zabbix_agent_server: "192.168.122.199"
```

##Insert on /etc/ansible/hosts
```bash
[zabbix-clients]
192.168.122.13
192.168.122.200
```


##How to run
```bash
ansible-playbook zabbix-agent.yml --limit zabbix-clients 
```
