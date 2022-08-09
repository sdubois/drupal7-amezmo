# Drupal 7 Amezmo

Instructions and helpful files for running Drupal 7 on the [Amezmo](http://amezmo.com) platform.

## Description

Drupal 7 requires some small modifications to make the most of Amezmo. This repo provides some files to make it easier to migrate your existing site to Amezmo.

## Files

###  composer.json

This file contains a list of PHP packages to be managed in composer. Amezmo only needs the [phpdotenv](https://github.com/vlucas/phpdotenv) package, but this can be used to add others if needed for your particular site.

This file should be placed in your root directory. 

### load.environment.php

This autoloaded file instructs Drupal to load environment variables from the .env file located on Amezmo.

This file should be placed in your root directory. 

### index.php

This is the standard index.php file that comes with any Drupal 7 installation, but with a minor modification to autoload code from composer packages. 

This file should replace the existing index.php file in your root directory. While it is generally an unwise idea to modify core, it is necessary in this case.

### settings.php

This is a very minimal settings.php file to demonstrate how to connect to your application's database on Amezmo using the provided environment variables. 

This can either be used as a starting point for your site, or a reference for modifying your existing settings.php file. 

In most cases, this file should be placed in the /sites/default directory. 

### .amezmo/after.pull

This script file is necessary to create a symlink to Amezmo's storage directory. For more information on deployment hooks, see the documentation at https://www.amezmo.com/docs/deployments/hooks

## Help

If you need assistance beyond the scope of this guide, contact Amezmo Support at https://www.amezmo.com/support

## Authors

Steven DuBois - [sdubois](https://github.com/sdubois)
