netbox-web
=========

Ensures that the [NetBox](http://netbox.readthedocs.io/) application is being proxied.

Role Variables
--------------

  - `netbox_install_directory`: /opt
  - `netbox_webserver_ssl_crt`: The contents of the SSL certificate
  - `netbox_webserver_ssl_key`: The contents of the SSL key
  - `netbox_webserver_use_ssl`: Default is `yes`

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
        - name: netbox-app
          netbox_install_directory: /srv
          netbox_webserver_ssl_crt: |
            -----BEGIN CERTIFICATE-----
            [cert]
            -----END CERTIFICATE-----
          netbox_webserver_ssl_key: |
            -----BEGIN PRIVATE KEY-----
            [key]
            -----END PRIVATE KEY-----

Dependencies
------------

Requires a PostgreSQL database and a running NetBox application. These can be installed with the `netbox-db` and `netbox-app` roles:

```
$ ansible-galaxy install straylight-project.netbox-db
$ ansible-galaxy install straylight-project.netbox-app
```

License
-------

Apache 2.0
