# ansible-sandbox

mac - 192.168.42.183

server-f01 - 192.168.42.70

desktop-f01 = 192.168.42.132

## create file /etc/ansible/hosts
and insert ip or hosts names for machine to control

```
192.168.42.70
192.168.42.132
```

## install sshd service on every machine
for ubuntu
```
sudo apt-get install ssh

cd ~/.ssh/

ssh-copy-id -i id_rsa.pub user@192.168.42.70
```

test first ansible command 
(-u user --sudo)
```
  ansible all -m ping -u user

ansible all -a "/bin/echo hello" -u user

ansible all -m copy -a 'src=print.py dest=~/print.py' -u user

```
## ansible playbook
```
   ansible-playbook playbook.yml -u user --sudo --ask-sudo-pass
```


