# abaptrial 1909
Install ABAP Trial 1909 using ansible

Usages: <br>
export HUBUSER="docker hub username" <br>
export HUBPASSWD="docker hub password" <br>
<code>  
ansible-playbook deployABAP1909.yml --extra-vars "docker_user=$HUBUSER docker_password=$HUBPASSWD"
</code>

# abaptrial 2022
Install ABAP Trial 2022 using ansible

Usages: <br>
export HUBUSER="docker hub username" <br>
export HUBPASSWD="docker hub password" <br>
<code>  
ansible-playbook deployABAP2022.yml --extra-vars "docker_user=$HUBUSER docker_password=$HUBPASSWD"
</code>
