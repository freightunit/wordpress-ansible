# Wordpress setup via Ansible

# Usage

    export RDS_USERNAME=<your db username>
    export RDS_PASSWORD=<your db password
    export RDS_DATABASE_NAME=<your database name>_prod
    ansible-playbook -i prod site.yml

# Idempotency

When creating instances, use the `id` to ensure idempotency to avoid creating multiple servers. When removing an instance and adding it again, this id needs to change, too.

    id: "{{ application }}-{{ item }}-1"

# TODO

* add NFS configuration so if you'd upload a wordpress plugin, 
  it's available on all hosts, to avoid missing files on the other hosts
* pull template changes from github
* install wordpress plugins required by the template
