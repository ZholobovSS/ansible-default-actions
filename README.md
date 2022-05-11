Ansible role: zh2s.default_actions
=========

Update repo, upgrade packages, reboot system (if needed) and install new packages from ansible variable `list_of_packages`


Role Variables
--------------

    list_of_packages: list of packages for installation


Example Playbook
----------------

    ---
    - hosts: all
      become: yes
      vars_files:
        - vars/main.yml

      roles:
        - { role: zh2s.create_user }

*Inside `vars/main.yml`*
-------

    list_of_packages: 
      - tree
      - htop
      - screen
      - wget