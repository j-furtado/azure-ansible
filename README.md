# azure-ansible
CI-CD infra deployment test with ansible and azure.

Requirements:
- Virtual box;
- Vagrant;

Steps to deploy:
- Generate a file named "credentials" on the same dir of the Vagranfile;
- Set the following structure:
[default]
subscription_id=<AZURE SUBSCRIPTION ID>
client_id=<AZURE CLIENT ID>
secret=<AZURE SECRET>
tenant=<AZURE TENANT>
- vagrant up -> it will deploy an Ubuntu VM with (hopefully) all the dependecies installed;
- vagrant ssh;
- ansible-playbook site.yml


TODO:
- Use ansible-vault for password management;
- Add password generation;
- Modularize the code (plenty of copy-paste now);
