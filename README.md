# Ansible Role: Apache Solr 5.4.1 for Drupal 7

This is a role to specifically install a version of Solr that is compatible with Drupal 7 AND the apachesolr AND search_api_solr modules.
As search_api_solar does not work with Solr 5.5 or later, the most recent version is 5.4.1, but a patch to that is required to access symlinks.
Therefore we have to compile from source.

At the time of writing this is very rough and ready, for example no /etc/init.d script is created and the compilation is not idempotent.

## Requirements

Java must be available on the server. You can easily install Java using the `geerlingguy.java` role. Make sure the Java version installed meets the minimum requirements of Solr (e.g. Java 8 for Solr 6+).

## Author

William Turrell <william@wturrell.co.uk> with some code from the `geerlingguy.solr` role (which you should use for more recent versions / where you don't need to compile from source).

https://github.com/geerlingguy/ansible-role-solr
