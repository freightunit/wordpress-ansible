# Wordpress setup via Ansible

# Usage

    export RDS_USERNAME=<your db username>
    export RDS_PASSWORD=<your db password
    export RDS_DATABASE_NAME=<your database name>_prod
    ansible-playbook -i prod site.yml

# TODO

* add NFS configuration so if you'd upload a wordpress plugin, it's available on all
  hosts, to avoid missing files on the other hosts

