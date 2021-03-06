#monasca-notification
Installs the [monasca-notification](https://github.com/stackforge/monasca-notification) part of the [Monasca](https://wiki.openstack.org/wiki/Monasca) project.

##Requirements
- kafka_hosts - comma seperate list of kafka hosts
- mysql_host
- mysql_user
- mysql_password
- smtp_host
- zookeeper_hosts - comma seperate list of zookeeper hosts

Optionally if needed
- smtp_user
- smtp_password
- mysql_ssl
  - This is a dictionary corresponding to the options in http://dev.mysql.com/doc/refman/5.0/en/mysql-ssl-set.html
  - For Example - {'ca':'/path/to/ca'}

##Example Playbook

    hosts: monasca
    sudo: yes
    roles:
      - {role: tkuhlman.monasca-notification,
         mysql_user: "{{notification_mysql_user}}",
         mysql_password: "{{notification_mysql_password}}",
         tags: [notification]}

##License
Apache

##Author Information
Tim Kuhlman
Monasca Team email monasca@lists.launchpad.net
