# ansible_endTB
ansible playbook to install bahmni(endTB) on a freshly installed centOS

Run playbook on a local server
--------------------------------

Install bahmni on a test server

cd /tmp

git clone https://github.com/PIH/ansible

cd ansible

chmod 755 installer.sh

./installAnsible.sh

ansible-playbook -e "target=localhost" test


setup a remote server using this playbook
------------------------------------------

cd /tmp

git clone https://github.com/PIH/ansible

cd ansible

ansible-playbook -u root --extra-vars="target=IP_Address" remote_test -k
