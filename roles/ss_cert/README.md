Self signed certificate
=========

Create self signed certificate with TLSv3

Requirements
------------

- Ubuntu 20.04
- Ubuntu 22.04

Role Variables
--------------

```
ss_cert_ca_key: ca.key
ss_cert_ca_path: ca.pem
ss_cert_ca_passphrase: null
ss_cert_key: cert-key.key
ss_cert_path: certificate.key
ss_cert_cn: "{{ ansible_host }}"
ss_cert_san: "{{ ss_cert_cn }}"
```


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: ss_cert, ss_cert_ca_key: /etc/keys/my-key.pem }

License
-------

BSD
