Role Name
=========

Installs mysql https://www.mysql.com/
Configurable options and cacti monitoring ready.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

````
cacti_db_user: cactiuser  #defines cacti db user for monitoring
cacti_db_password: cactiuser  #defines cacti db password for monitoring
cacti_server: cacti  #defines hostname of cacti server for monitoring
cacti_server_fqdn: 'cacti.{{ pri_domain_name }}'  #defines fqdn of cacti server for monitoring
enable_cacti_monitoring: false  #defines if cacti monitoring should be configured
deb_db_password:  #defines debian db password...generate using echo password | mkpasswd -s -m sha-512
mysql_allow_remote_connections: false  #defines if mysql should listen on loopback (default) or allow remove connections
mysql_port: 3306  #defines the port for mysql to listen on
mysql_root_password:  #defines mysql root password...generate using echo password | mkpasswd -s -m sha-512
pri_domain_name: example.org
````

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: mrlesmithjr.mysql }

License
-------

BSD

Author Information
------------------

Larry Smith Jr.
- @mrlesmithjr
- http://everythingshouldbevirtual.com
- mrlesmithjr [at] gmail.com
