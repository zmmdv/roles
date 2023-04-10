Ansible role for redis cluster from 6 nodes with autofailover

Playbook is default you don't have to change anything inside.

For initial playbook run type command ansible-playbook playbook.yml --tags all,never
that will start all processes to bootstrap your redis cluster.
!NOTE: you servers must be clean, because this playbook also starts os upgrade of all packages with this tags.

After install if you need to reconfigure your redis cluster type this command
 ansible-playbook playbook.yml --tags config
!NOTE: it will override your redis config on all machines and restart redis on all machines.

Predefined settings for redis clustger is located inside folder /files/redis.conf


This playbook only test on ubuntu 22.04 LTS in 13.03.2023

# I take no responsibility for your use of this role