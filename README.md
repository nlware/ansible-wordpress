## wordpress

[![Build Status](https://travis-ci.org/Oefenweb/ansible-wordpress.svg?branch=master)](https://travis-ci.org/Oefenweb/ansible-wordpress) [![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-wordpress-blue.svg)](https://galaxy.ansible.com/list#/roles/2600)

Set up wordpress (using `wp-cli`).

#### Requirements

* `php` (5.3.2+)
* `mysql` (5.0+)
* `apache2` (with `mod_rewrite` enabled)

This role assumes a working virtual host (that handles `wordpress_url`).

#### Variables

* `wordpress_wp_cli_install_dir` [default: `/usr/local/bin`]: Install directory for `wp-cli`

* `wordpress_installs`:
  * `name`: [default: `wordpress`]: Install name (not used for anything, just an identifier)
  * `dbname`: [default: `wordpress`]: Database name
  * `dbuser`: [default: `wordpress`]: Database username
  * `dbpass`: [default: `'heCrE7*d2KEs'`]: Database password (**make sure to change**)
  * `dbhost`: [default: `localhost`, optional]: Database host
  * `path`: [default: `/var/www`]: Install directory for wordpress
  * `url`: [default: `http://localhost`]: Wordpress url
  * `title`: [default: `wordpress`]: Wordpress title
  * `admin_name`: [default: `admin`, optional]: Wordpress admin (user)name
  * `admin_email`: [default: `root@localhost`]: Wordpress admin email address
  * `admin_password`: [default: `'tuFr8=aPra@a'`]: Wordpress admin password (**make sure to change**)
  * `themes`: [default: `[]`]: (Additional) themes to install (and activate)
  * `plugins`: [default: `[]`]: (Additional) plugins to install (and activate)

## Dependencies

None

#### Example

```yaml
---
- hosts: all
  roles:
  - wordpress
```

#### License

MIT

#### Author Information

Mischa ter Smitten

#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/Oefenweb/ansible-wordpress/issues)!
