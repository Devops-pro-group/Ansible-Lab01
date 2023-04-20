# Ansible-Lab01
# 1 Launch 3 ubuntu servers ( One Master and two slaves on AWS )
# 2  Remane the newly servers as the following : MasterAnsible Webservers Database
# 3 On the Master node :  ssh in to it and Install ansible ===>
       sudo apt update
       sudo apt install software-properties-common
       sudo add-apt-repository --yes --update ppa:ansible/ansible
       sudo apt install ansible
 # 4 On the MasteAnsible do ===> 
    sudo  cat /etc/ansible/hosts
    
