install_openmediavault_on_debian
=========

Install Openmediavault on Debian

Requirements
------------

You need a system with Debian 11 to install Openmediavault.

Role Variables
--------------

- `admin_password_hash`: if this variable is defined, we will use it to set the password for the system user `admin`

**Note**:
Changing user passwords in Ansible is not idempotent unless you
- specify the password hash or
- specify the password together with a so-called `salt`.

If you only specify the password, Ansible will report the task as changed each time, even though the password itself will not be changed.
https://docs.ansible.com/ansible/2.9/reference_appendices/faq.html#how-do-i-generate-encrypted-passwords-for-the-user-module

So, please only use a password hash as value for `admin_password_hash`.

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
        - { role: 'johanneskastl.install_openmediavault_on_debian' }

License
-------

BSD-3-Clause

Author Information
------------------

I am Johannes Kastl, reachable via kastl@b1-systems.de.
