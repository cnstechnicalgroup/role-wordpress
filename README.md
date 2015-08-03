Role: cns.wordpress
========

This role installs and configures WordPress.

Requirements
------------

Nothing, it runs out of the box.

Role Variables
--------------

In the current version, you can specify the following variables:

| Name                  | Default |                                                              |
|-----------------------|---------|--------------------------------------------------------------|
| admin_users           |   ---   | List containing all users that require ansible environment.  |
| wordpress_deploy_key |   ---   | git deploy key for site repository (use vault).              |
| web_root              |   ---   | Main root for wordpress install.                            |
| git_repo              |   ---   | Full git repository URL for site checkout.                   |
| mysql_server_hostname |   ---   | MySQL server host / proxy name.                              |
| wp_db_name            |   ---   | WordPress database name.                                    |
| wp_db_user            |   ---   | WordPress database usernem.                                 |
| wp_db_password        |   ---   | WordPress database password.                                |
| cache_system          |   ---   | WordPress cache system (File System, Memcached, APC, Xcache)|
| cache_enabled         |   ---   | Enable cache? 1=on, 0=off                                    |
| creation_date         |   ---   | Original deploy date.                                        |
| wp_version            |   ---   | Target WordPress version.                                   |
| site_public_url       |   ---   | Site URL. The primary site URL.                              |
| cdn_endpoint          |   ---   | Primary CDN end-point.                                       |
| cookie_key            |   ---   | Cookie blowfish key.                                         |
| cookie_iv             |   ---   | Cookie 8-letter IV.                                          |
| rijndael_key          |   ---   | Rijndael mcrypt key.                                         |
| rijndael_iv           |   ---   | Rijndael 8-letter IV.                                        |

Dependencies
------------

This package has no dependencies.

License
-------

GPLv2

Author Information
------------------

Created by Sam Morrison [@samcns](https://www.twitter.com/samcns)

Examples
--------

```yaml
---
- name: cns.wordpress role test
  hosts: all
  roles:
    - cns.wordpress
```
