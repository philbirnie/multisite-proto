# Multisite Prototype

This repository contains the seeds for a Wordpress site. :) 

## Author(s)

* **Phil Birnie** phil[at]7thstreeteweb.com
* **Sean Sefcik** sean[at]7thstreeteweb.com

## Setup 

### First time
* Seeder database files can be placed in the /mysql directory before starting docker and these will automatically be imported into your database. 

### Docker Integration
1.  After installing docker, you can run `docker-compose up` to re-constitute the site.  
2.  Connect to the MySQL server directly from your host machine using: 
    * Host: 127.0.0.1
    * User: wordpress
    * Password: wordpress
3. Note that the login and password can be changed in the `docker-compose.yml` file if desired

### Installing plugins

Keep all plugins that can be automatically installed in the `plugins.conf` file.  To install and activate all plugins in this file, simply run `docker-compose exec wordpress /var/www/html/plugins.sh`.  **This must be run AFTER the Wordpress installation has completed**  
    
### Accessing Components

1. After starting docker, the Wordpress installation will be available at localhost:8000 (current version of WP wll be automatically installed into `cms`)

### Site Development

1. Create you theme(s) in `cms/wp-content` after installation. Adjust the `.gitignore` file accordingly so that your theme isn't ignored. 

