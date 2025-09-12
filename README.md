# ansible
Set anisble Evironment
Generate SSH-KEY

ssh-keygen
~/.ssh/id_rsa

#copy ssh private to host that need to remote
ssh-copy-id -i ~/.ssh/anisible 192.168.9.80 
ssh-copy-id -i ~/.ssh/anisible 192.168.9.81 
ssh-copy-id -i ~/.ssh/anisible 192.168.9.82
echo "alias ssha='eval \$(ssh-agent) && ssh-add ~/.ssh/id_rsa'" >> ~/.bashrc

Create Inventory File

vim /home/ubuntu/ansible/inventory.txt
192.168.9.80
192.168.9.81
192.168.9.82

Create Ansible configure file 
vim /home/ubuntu/ansible/ansible.cfg
[default]
inventory = inventory.txt
private_key_file = ~/.ssh/id_rsa

I am testing add push to git hub
my website : https://sandgod.net

