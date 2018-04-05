# Ansible Role: MySQL Community Repository

Installs the MySQL Community repository for RHEL/CentOS, Fedora, Debian, and Ubuntu.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    mysql_repo_rpm_url: "https://repo.mysql.com/mysql57-community-release-{% if ansible_distribution == 'Fedora' %}fc{% else %}el{% endif %}{{ ansible_distribution_major_version }}.rpm"
    mysql_repo_deb_url: "https://repo.mysql.com/mysql-apt-config_0.8.9-1_all.deb"
    mysql_repo_key_url: "https://repo.mysql.com/RPM-GPG-KEY-mysql"
    mysql_repo_key_id:  "8C718D3B5072E1F5"

The MySQL Community repo URL and GPG key URL. Generally these should not be changed, but if this role is out of date or if you need a very specific version, these can both be overridden.

## Dependencies

None.

## Example Playbook

    - hosts: database
      roles:
        - rchouinard.mysql-community-repo

## License

MIT

## Author Information

This role was created in 2016 by [Ryan Chouinard](https://www.ryanchouinard.com/).
