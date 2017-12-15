Postfix
=======
An ansible role to install, configure, and maintain the postfix installation for Red Hat Enterprise Linux and Fedora


Postfix Requirements
--------------------
Supported Operating Systems:
  - Red Hat Enterprise Linux
  - CentOS
  - Fedora

We will accept pull requests to add in Debian, or Debian variants.

Variables
---------
* postfix: {}
* postfix_extra_options: {}

**Postfix Variables**
The following are appropriate keys for the postfix variable. Any postfix options not defined below should be placed into the **postfix_extra_options** variable for insertion into the configuration file.

* soft_bounce
* queue_directory
* command_directory
* daemon_directory
* data_directory
* mail_owner
* default_privs
* myhostname
* mydomain
* myorigin
* inet_interfaces
* inet_protocols
* proxy_interfaces
* mydestination
* local_recipient_maps
* unknown_local_recipient_reject_code
* mynetworks_style
* mynetworks
* relay_domains
* relayhost
* relay_recipient_maps
* in_flow_delay
* alias_maps
* alias_database
* recipient_delimiter
* home_mailbox
* mail_spool_directory
* mailbox_command
* mailbox_transport
* fallback_transport
* luser_relay
* header_checks
* fast_flush_domains
* smtpd_banner
* local_destination_concurrency_limit
* default_destination_concurrency_limit
* debug_peer_level
* debug_peer_list
* debugger_command
* sendmail_path
* newaliases_path
* mailq_path
* setgid_group
* html_directory
* manpage_directory
* sample_directory
* readme_directory

Dependencies
------------
No dependencies

Example Playbook
----------------

    - hosts: servers
      vars:
        postfix:
          relayhost: www.example.com
      roles:
         - { role: ISU-Ansible.postfix }

License
-------
GPLv2

Author Information
------------------
Barry Britt <bbritt@iastate.edu>
