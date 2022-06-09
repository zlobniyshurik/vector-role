zlobniyshurik.vector
=========

Install and enable **[Vector](https://vector.dev)**-service

Requirements
------------

Tested with `RHEL 8.x` clones.  

In theory can work with `Fedora` and `RHEL 9.x` (RPM-based OSes with **dnf** package manager)

Role Variables
--------------

***[defaults/main.yml](./defaults/main.yml)***
| Variables | Description | Default settings |
| :--------  | :----------   | :------------:  |
| **`vector_arch`** | Arch of `Vector` packages *(aarch64/armv7/x86_64)* | **x86_64** |
| **`vector_environment_file`** | Path to environment file | **`/etc/default/vector`** |
| **`vector_group`** | `Vector` group | **vector** |
| **`vector_rpm_build`** | Build of `Vector` RPM-packages | **1** |
| **`vector_user`** | `Vector` user | **vector** |
| **`vector_version`** | Version of `Vector` packages | **0.21.2** |


***[vars/main.yml](./vars/main.yml)***
| Variables | Description | Default settings |
| :--------  | :----------   | :------------  |
| **`vector_packages`** | List of installable `Vector` packages | <ul><li>vector</li></ul>  |

Dependencies
------------

No dependencies

Example Playbook
----------------

**playbook**

    - hosts: servers
      roles:
         - { role: zlobniyshurik.vector }

License
-------

MIT

Author Information
------------------

Alexander Dyadyun  
zlobniyshurik@gmail.com
