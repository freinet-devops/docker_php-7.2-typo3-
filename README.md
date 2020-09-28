# Usage
## php-fpm usage

Call without overriding entrypoint/command to run php-fpm in the foreground. Same as the base image php:7.1-alpine

## php-sshd usage
To run this as a companion container allowing access via ssgh to the webroot,
use

    command: ["/entrypoint-ssh.sh", "/usr/sbin/sshd", "-D", "-e"]

or

    entrypoint: "/entrypoint-ssh.sh" to start up
    command: ["/usr/sbin/sshd", "-D", "-e"]

to run the image as a companion