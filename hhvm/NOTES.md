# Introduction to HHVM

## What is HHVM?

HipHop Virtual Machine: Designed for executing programs written in Hack and PHP.

JIT Compilation: Compiles code on runtime. PHP is an interpreted language. With HHVM, PHP is compiled in order to increase the performance of your application.

Replacement for PHP-FPM: HHVM has support for FastCGI. Similar to PHP-FPM, HHVM can be ran as a socket or TCP address in which a web server can interact with.

Hack Language: Language similar to PHP. Not really that relevant.

## "Alternatives" to HHVM

PHP-NG: Latest HEAD in PHP. Refactored to optimize performance of PHP.

HippyVM: HippyVM is an implementation of the PHP language using RPython/PyPy technology.

Zephir: Compiles PHP code into C. Pretty much similar to PhalconPHP framework in which you load the framework as a PHP extension.

# Installation of Nginx, HHVM, and MySQL

Installation will be done on Ubuntu 12.04.

## Installation of Nginx and MySQL

There are no special steps when installation Nginx and MySQL.

## Installation of HHVM

Taken from the documentation. There is a PPA repository. Installation will be from pre-built packages.

`install_fastcgi.sh` determines the webserver you have installed and tries to configure it. In Nginx case, it adds the line `include hhvm.conf` on the default vhost.

# Configuration of Nginx, HHVM, and MySQL

## Configuration of HHVM

(show configuration of HHVM for `/etc/hhvm/php.ini` and `/etc/hhvm/server.ini` and emphasis on not needing to load extensions anymore)

## Configuration of Nginx

The `include hhvm.conf` is needed. The file simply consists of `fastcgi` options when the server runs the PHP scripts.

# Testing Performance of HHVM and PHP-FPM

`wrk` tool will be used since it's just a simple benchmark. No finetuning has been made on the configurations yet. The stack is a vanilla install with not much configuration made so there are a few things that will not work.

There are cases where the site would time out but both with HHVM and PHP-FPM.

(show benchmark)

# Demonstration

Show tests that don't work yet.

`sudo -u www-data drush test-run BlockCacheTestCase --methods=testCachePerRole --uri=http://hhvm-d7.dev`

`sudo -u www-data drush test-run BlockAdminThemeTestCase   --uri=http://hhvm-d7.devtest-run BlockAdminThemeTestCase   --uri=http://hhvm-`

# Conclusion

Better to get the test cases running first. Drupal HEAD is still currently on 99.98.
