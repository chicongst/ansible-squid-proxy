# Ensure Ansible is Installed
------------

## 1. Rename hosts.example to hosts
------------
Before starting, copy or rename the `hosts.example` file to hosts to use your server configuration.

```
cp hosts.example hosts
```

```
cp group_vars/all.example group_vars/all hosts
```

## 2. Ensure You Can SSH into the Listed IPs
------------

Make sure you can SSH into the IP addresses listed in the hosts file. 
[squid_servers]
1.2.3.4 ansible_user=ubuntu
```
If you are using a PEM key for SSH, ensure the hosts file is configured with the following syntax:
```
```
[squid_servers]
1.2.3.4 ansible_user=ubuntu ansible_ssh_private_key_file=/path/to/your-key.pem
```

## 3. Run the Ansible Playbook
------------

To execute the playbook, use the following command:
```
ansible-playbook -i hosts squid.yml
```

