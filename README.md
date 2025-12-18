# ansible-homelab

Ansible automation for managing my homelab infrastructure including Tailscale, Nginx Proxy Manager, and AdGuard Home.

Work in progress.

ANSIBLE COMMANDS
ansible all --key-file ~/.ssh/your-ansible-key -i inventory -m ping
add ansible.cfg and can shortened to "ansible all -m ping"

SHOW HOSTS
ansible all --list-hosts

SHOW ALL HOSTS INFO
ansible all -m gather_facts

SHOW SPECIFIC HOST INFO
ansible all -m gather_facts --limit SERVER_IP
