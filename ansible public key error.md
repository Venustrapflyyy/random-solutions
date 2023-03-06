- When your remote server refuses to be pinged by ansible, firstly check out the `/etc/ansible/ansible.cfg` file and edit it to contain
```
[defaults]
inventory = "path to your inventory"
remote_user = "your remote user"
private_key_file = "path to your public key.pem"
```
- then run the `ansible all -i "inventory" -m ping" command again. 
- This should work. 
