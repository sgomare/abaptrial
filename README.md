# General
These scripts require ansible; for Debian-based systems, use commonad apt install ansible.

# abaptrial 1909
Install ABAP Trial 1909 using Ansible.

Examples of usage:
<code>
export HUBUSER="Docker Hub Username"
export HUBPASSWD="docker hub password" 
ansible-playbook deployABAP1909.yml --extra-vars "docker_user=$HUBUSER, docker_password=$HUBPASSWD" 
</code>


# abaptrial 2022
Install ABAP Trial 2022 using Ansible.

Examples of usage:
<code>
export HUBUSER="Docker Hub Username"
export HUBPASSWD="docker hub password"  
ansible-playbook deployABAP2022.yml --extra-vars "docker_user=$HUBUSER, docker_password=$HUBPASSWD" 
</code>


# abaptrial 2022 LXC Special Instructions
1. The LXC container requires a further setting in the container configuration
   <code> features: keyctl=1,nesting=1</code>
3. The host Kernel requires the following parameters:
   <code>
   vm.max_map_count=2147483647
   fs.aio-max-number=18446744073709551615
   fs.file-max=20000000
   </code>
   If LXC is running in proxmox, add these arguments to /etc/sysctl.conf and execute the command <code> sysctl -p </code> then restart the container.

