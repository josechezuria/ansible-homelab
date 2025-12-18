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

TELL ANSIBLE TO USE SUDO (BECOME)
ansible all -m apt -a update_cache=true --become --ask-become-pass

INSTALL A PACKAGE VIA THE APT MODULE (VIM FOR EXAMPLE)
ansible all -m apt -a name=vim-nox --become --ask-become-pass

SUDO APT UPDATE && SUDO APT UPGRADE -Y
ansible all -m apt -a "update_cache=yes upgrade=yes" --become --ask-become-pass
