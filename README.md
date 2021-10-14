# Percona 2 Node CentOS 7 Ansible

# Usage
- cd `percona-1.0`
- Change node ips in hosts file
- Change variables in defaults (nodes, install)
- `ansible-playbook -i hosts site.yml`

# How to restart the cluster nodes

- In Node2 `systemctl stop mysql`
- In Node1 `systemctl stop mysql@bootstrap`
- Restart Nodes and start **mysql@bootstrap** in Node1 and **mysql** in Node2
