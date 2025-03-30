# Pull image only
ansible-playbook playbooks/docker-nginx.yml --tags pull

# Start container
ansible-playbook playbooks/docker-nginx.yml --tags start

# 🔄 Run necessery tasks except "remove" and "stop"
ansible-playbook playbooks/docker-nginx.yml --skip-tags "remove,stop"

# Stop container
ansible-playbook playbooks/docker-nginx.yml --tags stop

# Remove container
ansible-playbook playbooks/docker-nginx.yml --tags remove