Oh woe.

All variables are defined in ./inventory/group_vars/all.yml

Current Ansible version: core 2.14.6
Current k3s version: v1.27.2+k3s1
Designed for Ubuntu 22.04, x86_64.

*Before using*, install the requirements:

    ```ansible-galaxy collection install -r ./requirements.yml```

    ```pip-compile requirements.in```

*The whole thing is run with:*

    ```ansible-playbook playbook.yml --ask-pass --ask-become-pass```

After deployment control plane will be accessible via virtual ip-address which is defined in inventory/group_vars/all.yml as `apiserver_endpoint`. 