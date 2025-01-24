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







Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
