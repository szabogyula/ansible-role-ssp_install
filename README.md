# README.md
# Ansible Role: SimpleSAMLphp Installer

An Ansible role that installs SimpleSAMLphp

## Requirements

Once installed, configuration is needed for Service Provider (SP) or Identity Provider (IdP)

## Role Variables

Available variables are listed below, along with default values:

    ssp_ver: 1.14.4
    ssp_sha256: cf0fe8534c93be8073e70fa84556971711543293d4be65edb890335861d2e6b9
    ssp_url: https://simplesamlphp.org/res/downloads/simplesamlphp-{{ ssp_ver }}.tar.gz

    ssp_domain: localhost.local
    ssp_dir: /var/www/simplesamlphp-{{ ssp_ver }}
    ssp_tmp_dir: /tmp/ssp
    ssp_www_user: www-data
    ssp_www_group: www-data

    ssp_cron_enable: False
    ssp_refresh_key: secret

## Dependencies

None

## Example Playbook

    - hosts: idp
      roles:
        - { role: ssp_install }

## License


