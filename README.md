# PoolParty GitHub Backup Action
Scheduled PoolParty Concepts Backup using GitHub Actions

## How to configure

### Input variables
This action requires that you specify two input variables:
* `poolparty-instance-api-endpoint`
* `project-name`

You can do so by using the `width` keyword in the actions steps:

```yaml
steps:
  - uses: actions/checkout@v3
  - id: backup
    uses: actions/identifier-for-this-action@v1
    with:
      poolparty-instance-api-endpoint: 'https://poolparty.example.org/api/'
      project-name: 'yourprojectslug'
```


### Secret variables
This action requires two secrets to be added to the repository:
* `POOLPARTY_USERNAME`
* `POOLPARTY_PASSWORD`

These are credentials of a PoolParty API user and can be added via the repository's `Settings` --> `Secrets and Variables` --> `Actions` --> `Repository secrets` section.
