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

3. Select the peers to run it on in the blueprint wizard:

![Mautic Blueprint select peers](https://raw.githubusercontent.com/akarasulu/mautic-bp/master/bp-wizard2.png)


4. By default HTTPS will be used and the certificate will automatically be gotten from [letsencrypt](https://letsencrypt.org/), you can just click next. If you want to take a look just click the upload ssl keys button there to the right. It will show you the certs will be created with letsencrypt.

![Mautic Blueprint HTTPS and Certificates](https://raw.githubusercontent.com/akarasulu/mautic-bp/master/bp-wizard3.png)

Watch it build the environment for you. It will take a couple minutes.

![Mautic Blueprint Building](https://raw.githubusercontent.com/akarasulu/mautic-bp/master/bp-wizard4.png)


If you're impatient like me you can check the logs by going to the `Application` tab to select the logs button for the Mautic application. NOTE: you can install Muatic into existing cloud environments next to other applications as well.

![Mautic Blueprint Building](https://raw.githubusercontent.com/akarasulu/mautic-bp/master/bp-wizard5.png)


5. After building successfully go the following URL (put in your domain):

```
https://$yourdomain/index.php/installer
```

6. You will be on the installer for Mautic which will ask for Database and Mail configuration questions. Here's the answer to the questions:

* mail host: localhost
* mail port: 25
* mail password/security: none
* db user: mautic
* db name: mautic
* db password: mautic

Anything else feel free to ask.
