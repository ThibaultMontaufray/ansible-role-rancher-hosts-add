RANCHER ADD HOST
================

This roles add hosts in rancher

Example Playbook
----------------

Here is a use case :

```yaml
  - hosts: servers
    remote_user: mysuperadmin
    vars:
     - rancher_api_key: "admin"
     - rancher_api_secret: "r@nch3r!"
     - rancher_master_url: "http://{{ hostmaster }}:8080"
     - rancher_project_name: "myproject"
     - custom_host_tags: "master=true&slave=false"
     - rancher_agent_version: "v1.2.11"
     - rancher_project_id: "{{ rancher_pj.rancher_project_id }}"
    roles:
      - ansible-role-rancher-add-hosts
```

License
-------

MIT
