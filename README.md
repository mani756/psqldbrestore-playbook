Requirements:

In the source machine:

Install Ansible

SSH action to destination machine

In the remote machine:

Install and configure PostgreSQL follow the below link for installation steps

http://www.thegeekstuff.com/2009/04/linux-postgresql-install-and-configure-from-source/

Instructions:

Configure playbook by modifying hosts.ini file and vars.yml file.

hosts.ini:



 
Vars.yml:


remote_bk_dir = path in which we need to take backup

db_name= database name which we need to take backup

db_user= database user name

Run it by using below command:

ansible-playbook --inventory-file=hosts.ini psqlbackup.yml


After running the playbook validate it in remote host:
 
fileformat_poc_dump_20160624-062452.sql.gz: The backup data is stored in this file.
