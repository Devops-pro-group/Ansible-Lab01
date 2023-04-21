# Ansible-Lab01
# 1 Launch 3 ubuntu servers ( One Master and two slaves on AWS )
# 2  Remane the newly servers as the following : MasterAnsible Webservers Database
# 3 On the Master node :  ssh in to it and Install ansible ===>
       sudo apt update
       sudo apt install software-properties-common
       sudo add-apt-repository --yes --update ppa:ansible/ansible
       sudo apt install ansible
 # 4 On the MasteAnsible do ===> 
     mkdir /var/myansible/
     Copy your key pair  on this directory ==>  /var/myansible/
     sudo chmod 400 yourkey.pem 
    sudo  vi /etc/ansible/hosts
    [web]
    webserversipAdress ansible_user=ubuntu  ansible_ssh_private_key_file= /var/myansible/youkeyName.pem
    [databases]
    databaseIpd ansible_user=ubuntu  ansible_ssh_private_key_file= /var/myansible/youkeyName.pem
  # 5 Check to see if MasterAnsible can talk to its slaves nodes
     ansible all -m ping 
  # Now let learn how to create a roles  from scratch : NB it could be achievable by ansible-galaxy but we want to be more familiar with roles with small tasks 
        # create three folders 
          mkdir roles
              mkdir nginx
                 mkdir tasks
                    touch main.yml
     # Create your plabook file outside of these above folders 
         touch nginx.yml 
           
    
