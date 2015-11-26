# README.md
# Ansible Role: mats116.hhvm

An Ansible role that installs HHVM on **Ubuntu 14.04 LTS**

## Requirements

none

## Role Variables

Available variables are listed below, along with default values:

    hhvm_version: "3.10"

    # server.ini
    hhvm_pidfile: /var/run/hhvm/pid

    hhvm_server_port: 9000
    hhvm_server_type: fastcgi
    hhvm_server_default_document: index.php
    hhvm_log_use_log_file: "true"
    hhvm_log_file: /var/log/hhvm/error.log
    hhvm_repo_central_path: /var/run/hhvm/hhvm.hhbc

    # php.ini
    session_save_handler: files
    session_save_path: /var/lib/hhvm/sessions
    session_gc_maxlifetime: 1440

    hhvm_log_level: Warning
    hhvm_log_always_log_unhandled_exceptions: "true"
    hhvm_log_runtime_error_reporting_level: 8191
    hhvm_mysql_typed_results: "false"

## Dependencies

none

## Example Playbook

    - hosts: web-server
      roles:
        - role: mats116.hhvm
          hhvm_server_port: 8080

## License

MIT
