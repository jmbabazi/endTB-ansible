# ansible_endTB
ansible playbook to install bahmni(endTB) on a freshly installed centOS

Vagrant
-------
To set up your vagrant box, download the Vagrantfile and in the same directory as the Vagrantfile do:

vagrant up

Run playbook on a local server
--------------------------------

Install bahmni on a test server

cd /tmp

git clone https://github.com/PIH/ansible

cd ansible

chmod 755 installer.sh

./installAnsible.sh

ansible-playbook -e "target=localhost" test


setup a remote server running this playbook on your local machine
------------------------------------------------------------------

install the sshpass program

add remote_ip-address in /etc/ansible/hosts

cd /tmp

git clone https://github.com/PIH/ansible

cd ansible

ansible-playbook -u root --extra-vars="target=remote_IP_Address" remote_test.yml -k
