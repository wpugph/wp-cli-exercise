# WordPress CLI Exercise

## Prerequisites:

- A local development environment of you choice (eg. XAMPP)

Download a suitable version for your OS: https://www.apachefriends.org/download.html

- Composer 
  
```
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php -r "if (hash_file('SHA384', 'composer-setup.php') === '544e09ee996cdf60ece3804abc52599c22b1f40f4323403c44d44fdfdd586475ca9813a858088ffbc1f233e9b180f061') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"
```

mv composer.phar /usr/local/bin/composer


## Bedrock installation

1. Create a new project - composer create-project roots/bedrock
2. Copy .env.example to .env and update environment variables:

```
  DB_NAME - Database name
  DB_USER - Database user 
  DB_PASSWORD - Database password
  DB_HOST - Database host
  WP_ENV - Set to environment (development, staging, production)
  WP_HOME - Full URL to WordPress home (http://example.com)
  WP_SITEURL - Full URL to WordPress including subdirectory (http://example.com/wp)
  AUTH_KEY, SECURE_AUTH_KEY, LOGGED_IN_KEY, NONCE_KEY, AUTH_SALT, SECURE_AUTH_SALT, LOGGED_IN_SALT, NONCE_SALT - Generate with wp-cli-dotenv-command or from the Roots WordPress Salt Generator
```  
3. Add theme(s) in web/app/themes as you would for a normal WordPress site.
4.  your site vhost document root to /path/to/site/web/ (/path/to/site/current/web/ if using deploys)
5. Access WP admin at http://example.com/wp/wp-admin

* Might need to setup your DB creds
