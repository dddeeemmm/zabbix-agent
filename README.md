zabbix-agent
=========

    Install and configure zabbix-agent

Role Variables
--------------

    zabbix_agent_install: ''        [ default: true ] install packages

    zabbix_agent_host_metadata: ''  [ not required ] host metadata
    zabbix_agent_log_file_size: ''  [ default: 128 ] log file size
    
    nolog: ''                       [ default: true ] disable log secrets

Example Playbook
----------------

    - hosts: servers
      become: true
      vars:
        zabbix_agent_host_metadata: k8s
      roles:
        - { name: zabbix-agent, tags: [ zabbix ] }

License
-------

    MIT

Author Information
------------------

    Dmitrij Petrov
