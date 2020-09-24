---
layout: page
title: MYSQL
permalink: /mysql/
nav_order: 6
---

# MySQL for WordPress

***Find the rows with the largest amount of data in the option_value***

<code>SELECT option_name, length(option_value) FROM wp_options WHERE autoload='yes' ORDER BY length(option_value) DESC LIMIT 30</code>

***Find meta_keys causing bloat***

<code>SELECT substring(meta_key, 1, 20) AS key_start, count(*) AS count FROM wp_postmeta GROUP BY key_start ORDER BY count DESC LIMIT 30</code>

# Advanced MySQL

## Indexes

- [MySQL Index](https://www.mysqltutorial.org/mysql-index/)

## Foreign Keys

WordPress does not support foreign keys out of the box, with that said you may want to configure it for some of the default tables, and any custom tables.

- [MySQL Foreign Keys](https://www.mysqltutorial.org/mysql-foreign-key/)
- [WordPress screams for Foreign Keys](https://petermolnar.net/article/wordpress-innodb-screams-for-foreign-keys/)
- [Foreign Keys Help Performance](https://www.scarydba.com/2015/09/09/yes-foreign-keys-help-performance/)

## Stored Functions

- [Stored Functions](https://www.mysqltutorial.org/mysql-stored-function/)

## Triggers

- [How to Create MySQL Triggers](https://www.sitepoint.com/how-to-create-mysql-triggers/)
- [MySQL Triggers](https://www.mysqltutorial.org/mysql-triggers.aspx)
