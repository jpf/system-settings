This is the set of Ansible playbooks that I use to manage my OS X
workstations. Initial setup (that requires root) is in the
setup-osx.yml file. My day-to-day configuration is in default.yml.


SETUP:

$ sudo easy_install pip
$ sudo ARCHFLAGS=-Wno-error=unused-command-line-argument-hard-error-in-future pip install paramiko PyYAML jinja2 httplib2
$ ansible-playbook -K -i inventory setup-osx.yml
$ ansible-playbook -i inventory default.yml

NORMAL USE:

Once I've setup Ansible, all of my changes are done to default.yml,
which is run with the following command:

$ ansible-playbook -i inventory default.yml
 
