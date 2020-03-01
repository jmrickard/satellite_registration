# Role Purpose
The purpose of this role is to register a Red Hat machine to an existing satellite service. 

# Variables
**Name**|**Default Value**|**Purpose**|
------|------|------|
|satellite_fqdn|empty|Put satellite fully-qualified hostname here|
|org_id|empty|Enter the Satellite organization name|
|activationkey|rhel|Enter the activationkey to use for registration|

# Create a playbook that runs the role:
`vim register.yml`
```
- name: Register machine to Satellite
  hosts: all
  remote_user: root
  roles:
    - machine_register_satellite
```

# How to use this role
`ansible-playbook register.yml`
