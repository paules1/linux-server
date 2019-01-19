# Linux Server Project
### Server Properties
* 512 MB RAM
* 1 vCPU
* 20 GB SSD
* Location: Virginia Zone
* Distribution: Ubuntu
* IP: 3.90.124.238
* SSH port: 2200
* HTTP port: 80

### Software Installed
* Finger
* Python2
* Pip2
* Python Modules
    * Flask
    * OAuthClient2
    * SqlAlchemy
* Apache2
   * WSGI package
* Postgresql
* Git
* Catalog App

### Configurations
* Server
   * Changed ssh port from 22 to 2200
   * Enabled firewall to allow traffic on port 2200, 80, and 123 only.
   * Disabled root ssh access
   * Allowed only Key-based SSH authentication
* Postgresql
   * Modified /etc/postgresql/9.5/main/postgresql.conf to allow local access only.
   * Created "catalog" user and granted privileges for "catalog" database only.
* Apache2
   * Created application.wsgi file that imports and executes the python catalog application
   * Modified etc/apache2/sites-available/000-default.conf to make application.wsgi the single entry point and set the execution user. 
* Catalog App
   * Updated connection string with catalog database and user credentials.

### Application Hosted
Car Catalog App
* http://www.3.90.124.238.xip.io

### Third party resources
* http://flask.pocoo.org/docs/1.0/deploying/mod_wsgi/
* https://flask-cors.readthedocs.io/en/latest/
* https://developers.google.com/api-client-library/python/guide/aaa_oauth
* https://www.postgresql.org/docs/9.1/app-createuser.html

### Project Status
* Submitted
