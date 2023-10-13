# ansible-roboshop

#ansible collection is group of modules
#commands- ansible -i /tmp/inv all -e ansible_user=centos -e ansible_password=DevOps321 -m ansible.builtin.ping
ansible -i 172.31.50.183, all -e ansible_user=centos -e ansible_password=DevOps321 -m ansible.builtin.ping
/tmp/inv
[APP]
172.31.50.183
[DB]
172.31.50.184

ansible -i /tmp/inv APP -e ansible_user=centos -e ansible_password=DevOps321 -m ansible.builtin.ping
OUTPUT:
172.31.50.183 | SUCCESS => {
    "ansible_facts": {
        "discovered_interpreter_python": "/usr/libexec/platform-python"
    },
    "changed": false,
    "ping": "pong"
}

52.87.176.96 | 172.31.83.101 | t3.medium | null

dynamic inverntoy creation:
aws ec2 describe-instances | jq '.Reservations[].Instances[].PrivateIpAddress' >/tmp/inv

Adhoc commands
ansible -i /tmp/inv APP -e ansible_user=centos -e ansible_password=DevOps321 -bm yum -a "name=nginx"

Ansible
Key-value-Plain
Key-Multiple Values -LIST
KEY-KEY-VALUE- MAP

Ansible Playbook
#Playbook has multiple plays
#playbook file itself is a LIST
#playbook should have atleast one play
#play must have info about the inventory resource group(hosts) based on that it should load tasks and roles.

Ansible variables

1. Play level variables - 
