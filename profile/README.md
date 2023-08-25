# Jail templates for Bastille
FreeBSD jails make OS-level virtualization possible by creating multiple user-space instances that can be isolated from the rest of the operating system. Jails add a lot of flexibility and enhance security without adding much overhead.

[Bastille](https://bastillebsd.org/) is a great open-source manager for deploying and managing jails. We love it because it's efficient and fast, has a great featureset and is easily extendable because of its low complexity design. One of those great features is support for [templates](https://bastille.readthedocs.io/en/latest/chapters/template.html) and that's where we come in to play.

Templates are flexible rules that can be applied to jails, for example to install and configure software, copy data and execute commands. We created templates for the packages we use ourselves and thought it would be nice to share them. What sets these templates apart from the templates offered by Bastille is a sane default configuration that follows security best practices. Template details are listed in each template repository's README.

## Getting started
A template needs to be bootstrapped by Bastille before it can be used. Bootstrap a template by running:
```
bastille bootstrap https://github.com/jail-templates/$TEMPLATE
```
After bootstrapping the template can be applied by running:
```
bastille template $JAIL jail-templates/$TEMPLATE
```

## Templates
### Meta-templates
Meta-templates do not contain any template logic by themselves, but consist of two or more templates for ease of use. For example, instead of applying the `apache-https`, `mariadb` and `php` templates in sequence, you could just apply the `famp-https` meta-template instead.

The `meta` meta-template is special: it consists of *all* available templates. This is helpful for bootstrapping all available templates at once, but shouldn't be applied to containers.

| Meta template | Repository | Description |
| ------------- | ---------- | ----------- |
| all | https://github.com/jail-templates/all | Bootstrap all available templates.<br>- https://github.com/jail-templates/basics<br>- https://github.com/jail-templates/vnstat<br>- https://github.com/jail-templates/apache-http<br>- https://github.com/jail-templates/apache-https<br>- https://github.com/jail-templates/php<br>- https://github.com/jail-templates/php-8.0<br>- https://github.com/jail-templates/php-8.1<br>- https://github.com/jail-templates/php-8.2<br>- https://github.com/jail-templates/php-8.3<br>- https://github.com/jail-templates/mariadb<br>- https://github.com/jail-templates/mariadb-10.5<br>- https://github.com/jail-templates/mariadb-10.6<br>- https://github.com/jail-templates/mariadb-10.11<br>- https://github.com/jail-templates/famp-http<br>- https://github.com/jail-templates/famp-https |
| famp-http | https://github.com/jail-templates/famp-http |  Install and configure a full FAMP server.<br>- https://github.com/jail-templates/apache-http<br>- https://github.com/jail-templates/mariadb<br>- https://github.com/jail-templates/php |
| famp-https | https://github.com/jail-templates/famp-https |  Install and configure a full FAMP server.<br>- https://github.com/jail-templates/apache-https<br>- https://github.com/jail-templates/mariadb<br>- https://github.com/jail-templates/php |

### Apache templates
| Template | Repository | Description |
| -------- | ---------- | ----------- |
| apache-http | https://github.com/jail-templates/apache-http | Install and configure the Apache HTTP Server (HTTP-only). |
| apache-https | https://github.com/jail-templates/apache-https | Install and configure the Apache HTTP Server (HTTP/HTTPS). |

### PHP templates
| Template | Repository | Description |
| -------- | ---------- | ----------- |
| php | https://github.com/jail-templates/php | Install and configure the latest stable PHP. |
| php-8.0 | https://github.com/jail-templates/php-8.0 | Install and configure PHP 8.0. |
| php-8.1 | https://github.com/jail-templates/php-8.1 | Install and configure PHP 8.1. |
| php-8.2 | https://github.com/jail-templates/php-8.2 | Install and configure PHP 8.2. |
| php-8.3 | https://github.com/jail-templates/php-8.3 | Install and configure PHP 8.3. |

### MySQL templates
| Template | Repository | Description |
| -------- | ---------- | ----------- |
| mariadb | https://github.com/jail-templates/mariadb | Install and configure the latest stable MariaDB Server. |
| mariadb-10.5 | https://github.com/jail-templates/mariadb-10.5 | Install and configure MariaDB Server 10.5. |
| mariadb-10.6 | https://github.com/jail-templates/mariadb-10.6 | Install and configure MariaDB Server 10.6. |
| mariadb-10.11 | https://github.com/jail-templates/mariadb-10.11 | Install and configure MariaDB Server 10.11. |

### Other templates
| Template | Repository | Description |
| -------- | ---------- | ----------- |
| basics | https://github.com/jail-templates/basics | Install some basic apps and supress the MOTD. |
| vnstat | https://github.com/jail-templates/vnstat | Install vnStat and set `/var/db/vnstat` correctly. |
| wordpress | https://github.com/jail-templates/wordpress | Install, configure and harden WordPress. |

## Support
Templates will be maintained until their respective software version is end-of-life. Repositories will then be archived and removed from any meta-templates.

If you have a question, suggestion or find a bug, please let us know via an Issues in the relevant repository or send us an email.

## License
All templates are distributed under the 3-Clause BSD License. See `LICENSE` in every template repository for more information.
