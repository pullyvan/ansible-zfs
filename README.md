Role ZFS Dataset
=========

Ansible role to install silently ZFS 6.8 with licenses.

Compatibility
------------

This role can be used on Ubuntu 18. Other OS will come later

Variables Used
------------

You can find in defaults/main.yml all variables used in tasks

| Variable                 | Default Value                                                | Type   | Description                                                  |
| ------------------------ | :----------------------------------------------------------- | :----- | ------------------------------------------------------------ |
| fstype     | ZFS    | String | File System                                                    |
| dev   | /dev/nvme0n1                                                       | String | Default Device for ZFS Dataset                         |
| mount          | /home                                                            | String   | Default mountpoint |
| opts                      | rw                                                   | String | Default access Read / write                          |
| state                 | mounted                                                            | String | Default mount state                 |

## Author Information

Written by [Pullyvan Krishnamoorthy ](mailto:pullyvan.krishnamoorthy@epfl.ch) 
=======

Role Name
=======

The ZFS role created and mount zfs as home directory, please specify the device in the pool in task/main.yml.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: all
      roles:
         - { role: roles/zfs-dataset }

License
-------

BSD
