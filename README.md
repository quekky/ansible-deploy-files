deploy-files
============

Generic role to deploy files to a server. It can be optionally backup the existing files to a dir on the server.
The role will compare the files and copy only the files that have changed, as well as backup only the files that have changed between src and dest.

Requirements
------------

This role requires Ansible 2.0 or higher.

Role Variables
--------------

The variables that can be passed to this role and a brief description about them are as follows.

	src:
	dest:
	remote_src: false
	backup_dir:


Dependencies
------------

None

Example Playbook
----------------

Deploy the localhost file abc.htm to the website:

    - hosts: servers
      roles:
        - role: quekky.deploy-files
          src: /home/abc.htm
          dest: /var/www/html/

Deploy all the localhost files in the dir /todeploy/ to the website, backup existing files to /backup/:

    - hosts: servers
      roles:
        - role: quekky.deploy-files
          src: /todeploy/
          dest: /var/www/html/
          backup_dir: /backup

License
-------

MIT

Author Information
------------------

quekky
