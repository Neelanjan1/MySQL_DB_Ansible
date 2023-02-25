# We can directly give the username and password in the playbook file however that is not a recommended way.
# Another method, to encrypt the yaml file and use a separate file to store the vault password.
'''
Command - ansible-vault encrypt mysql_db.yml
this command will ask for password setup which you can store in a different file e.g., vault_pass.txt
ansible-playbook mysql_db.yml --vault-password-file ~/.vault_pass.txt
Details - https://docs.ansible.com/ansible/2.9/user_guide/playbooks_vault.html
'''
# Another method, use a different file say - secret.yml
'''
ansible-playbook mysql_db.yml -e@secret.yml
'''