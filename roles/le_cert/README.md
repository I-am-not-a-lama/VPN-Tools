Lets Encrypt signer
=========
The role get let`s encrypt certificate for domain

Requirements
------------

- Ubuntu 20.04
- Ubuntu 22.04

Role Variables
--------------
```
domain_name: your-domain # Doesn`t have default
le_cert_acme_email: certificate-reminders@your-domain # Doesn`t have default
le_cert_site_directory: /var/www/html
le_cert_acme_challenge_type: http-01
le_cert_acme_challenge_directory: "{{ le_cert_site_directory }}/.well-known/acme-challenge"
le_cert_acme_directory: https://acme-v02.api.letsencrypt.org/directory
le_cert_acme_version: 2
le_cert_dir: /etc/letsencrypt
le_cert_keys_dir: /etc/letsencrypt/keys
le_cert_csrs_dir: /etc/letsencrypt/csrs
le_cert_certs_dir: /etc/letsencrypt/certs
le_cert_account_key: /etc/letsencrypt/account/account.key
```

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: le_cert, le_cert_acme_email: admin@somedomain.freemyip.com, domain_name: somedomain.freemyip.com }

License
-------

BSD
