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

dynamic inverntoy creation
aws ec2 describe-instances | jq '.Reservations[].Instances[].PrivateIpAddress' >/tmp/inv

ansible -i /tmp/inv APP -e ansible_user=centos -e ansible_password=DevOps321 -bm yum -a "name=nginx"