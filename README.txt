sudo easy_install pip
sudo ARCHFLAGS=-Wno-error=unused-command-line-argument-hard-error-in-future pip install paramiko PyYAML jinja2 httplib2
ansible-playbook -i inventory default.yml
