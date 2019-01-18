# Mautic

A blueprint for creating a mautic installation.

## How to use

1. On the Subutai Bazaar just build the Mautic Blueprint

![Mautic Blueprint on Bazaar](https://raw.githubusercontent.com/akarasulu/mautic-bp/master/bazaar.png)

2. The Subutai Blueprint Wizard will ask a few questions needed to install the application properly:

![Mautic Blueprint on Bazaar](https://raw.githubusercontent.com/akarasulu/mautic-bp/master/bp-wizard.png)

* hostname is the name of the container running mautic, the mariadb is installed in this same container
* password is the password for the database user
* mautic is automatically the name of the database user and db name in mariadb
* the email is optional but nice to have since admin issues will be emailed to this user
* medium is a good size

The rest is not all that important.


3. After building successfully go the following URL (put in your domain):

```
https://$yourdomain/index.php/installer
```

4. You will be on the installer for Mautic which will ask for Database and Mail configuration questions. Here's the answer to the questions:

* mail host: localhost
* mail port: 25
* mail password/security: none
* db user: mautic
* db name: mautic
* db password: mautic

Anything else feel free to ask.
