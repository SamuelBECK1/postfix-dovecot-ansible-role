Role Name
=========

Install and configure together Postfix / Dovecot and OpenDKIM On Debian or Ubuntu

Requirements
------------

- Following ports must be open:  
80/tcp => only during installation (required for letsencrypt http challenge)  
25/tcp 587/TCP => SMTP  
143/tcp => IMAP  

- Valid domain name with a hostname pointing to your server.


Role Variables
--------------
all variables are listed in the defaults values (default/main.yml)  
```
POSTFIX_CSR_DN_C: FR
POSTFIX_CSR_DN_ST: FR
POSTFIX_CSR_DN_L: Paris
POSTFIX_CSR_DN_O: TEST
POSTFIX_CSR_DN_OU: EXAMPLE
POSTFIX_CSR_DN_EMAILADDRESS: test@example.com
```
definition of the csr DN if POSTFIX_TLS_USE_CERTBOT is true  

```
POSTFIX_USERS:
  - USERNAME: example
    PASSWORD: changeme
```
list of users (mail address will be example@yourdomain.tld in this case)   








Example Playbook
----------------

```
- hosts: all
  roles:
  - name: postfix-dovecot-ansible-role
```

License
-------

BSD
