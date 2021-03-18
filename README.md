# Ansible_testwork

### Description:
This Project designed for use in multi-environment.
Parameters of servers located in `inventories` directory. Environment inventory split to `dev`, `stage`, `prod`.

### This Ansible project doing:
1. Install PostgreSQL with import demo dump
2. Setup docker on servers with Ubuntu or CentOS
3. Prepare servers to using Nginx. 
4. Create example "Hello" sites for Nginx
5. Run Nginx in Docker (nginx:latest) on prepared servers

### Verified OS:
 - Ubuntu 18.04
 - CentOS 8

### Before use:
You must to set your servers in `inventory` in matched directories.
Example you can see in file `./inventories/dev/inventory`

## How to use:

### Example command to full install. Use in root of repository:

    ansible-playbook  -i inventories/dev/inventory playbooks/full_install.yml

### Or you can execute playbooks only for your needs:
 - install-postgres.yml - for installation PostgreSQL and import demo dump
 - start-nginx.yml - for setup docker, prepare nginx config and sites, run nginx in docker
 - create_users.yml - for create Linux users

