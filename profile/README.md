# Jail templates with sane defaults for Bastille
In this 

## Meta-templates
Meta-templates do not contain any template logic by themselves, but consist of two or more templates for ease of use. For example, instead of applying the `apache-https`, `mariadb` and `php` templates in sequence, you could just apply the `famp-https` meta-template instead.

The `meta` meta-template is special: it consists of *all* available templates. This is helpful for bootstrapping all available templates at once, but shouldn't be applied to containers.

| Meta template | Repository | Description |
| ------------- | ---------- | ----------- |
| meta | https://github.com/jail-templates/meta | Bastille meta-template for bootstrapping all available templates.<br>- https://github.com/jail-templates/basics<br>- https://github.com/jail-templates/vnstat<br>- https://github.com/jail-templates/apache-http<br>- https://github.com/jail-templates/apache-https<br>- https://github.com/jail-templates/php<br>- https://github.com/jail-templates/php-8.0<br>- https://github.com/jail-templates/php-8.1<br>- https://github.com/jail-templates/php-8.2<br>- https://github.com/jail-templates/php-8.3<br>- https://github.com/jail-templates/mariadb<br>- https://github.com/jail-templates/mariadb-10.5<br>- https://github.com/jail-templates/mariadb-10.6<br>- https://github.com/jail-templates/mariadb-10.11<br>- https://github.com/jail-templates/famp-http<br>- https://github.com/jail-templates/famp-https |
| famp-http | https://github.com/jail-templates/famp-http |  Bastille meta-template to install and configure a full FAMP server with some sane defaults.<br>- https://github.com/jail-templates/apache-http<br>- https://github.com/jail-templates/mariadb<br>- https://github.com/jail-templates/php |
| famp-https | https://github.com/jail-templates/famp-https |  Bastille meta-template to install and configure a full FAMP server with some sane defaults.<br>- https://github.com/jail-templates/apache-https<br>- https://github.com/jail-templates/mariadb<br>- https://github.com/jail-templates/php |

## Apache templates
| Template | Repository | Description |
| -------- | ---------- | ----------- |
| apache-http | https://github.com/jail-templates/apache-http | Bastille template to install and configure the Apache HTTP server (http-only) with some sane defaults. |
| apache-https | https://github.com/jail-templates/apache-https | Bastille template to install and configure the Apache HTTP server (http/https) with some sane defaults. |

## PHP templates
| Template | Repository | Description |
| -------- | ---------- | ----------- |
| php | https://github.com/jail-templates/php | Bastille template to install and configure the latest stable PHP with some sane defaults. |
| php-8.0 | https://github.com/jail-templates/php | Bastille template to install and configure the PHP 8.0 with some sane defaults. |
| php-8.1 | https://github.com/jail-templates/php | Bastille template to install and configure the PHP 8.1 with some sane defaults. |
| php-8.2 | https://github.com/jail-templates/php | Bastille template to install and configure the PHP 8.2 with some sane defaults. |
| php-8.3 | https://github.com/jail-templates/php | Bastille template to install and configure the PHP 8.3 with some sane defaults. |

## MySQL templates
| Template | Repository | Description |
| -------- | ---------- | ----------- |
| mariadb | https://github.com/jail-templates/mariadb | Bastille template to install and configure the latest stable MariaDB Server with some sane defaults. |
| mariadb-10.5 | https://github.com/jail-templates/mariadb | Bastille template to install and configure MariaDB Server 10.5 with some sane defaults. |
| mariadb-10.6 | https://github.com/jail-templates/mariadb | Bastille template to install and configure MariaDB Server 10.6 with some sane defaults. |
| mariadb-10.11 | https://github.com/jail-templates/mariadb | Bastille template to install and configure MariaDB Server 10.11 with some sane defaults. |

## Support
Templates will be maintained until their respective software version is end-of-life. Repositories will then be archived and removed from any meta-templates.

If you have a question, suggestion or find a bug, please let us know via an Issues in the relevant repository.

## Contact
You can contact us on 

### License & copyright