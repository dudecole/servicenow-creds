# servicenow-creds

## Custom Credential

### Custom Credential Configuration

Input Configuration
```yaml
fields:
  - id: sn_username
    type: string
    label: ServiceNow Username
    secret: false
  - id: sn_password
    type: string
    label: ServiceNow Password
    secret: true
  - id: sn_host
    type: string
    label: ServiceNow Host
    secret: false
required:
  - sn_username
  - sn_password
  - sn_host


```

Injector configuration
```yaml
env:
  SN_HOST: '{{ sn_host }}'
  SN_PASSWORD: '{{ sn_password }}'
  SN_USERNAME: '{{ sn_username }}'
```
