# PoolParty GitHub Backup Action
Scheduled PoolParty Concepts Backup using GitHub Actions

## How to configure

### Input variables
This action requires that you specify three input variables:
* `poolparty-instance-api-endpoint`
* `project-name`
* `target-filepath`

:warning: For the `target-filepath` variable, it assumes that this file is already present in the repository and therefore tracked in the git version tree. This can also be an empty file to start with.

You can specify these variables by using the `width` keyword in the actions steps:

```yaml
steps:
  - uses: actions/checkout@v3
  - id: backup
    uses: actions/identifier-for-this-action@v1
    with:
      poolparty-instance-api-endpoint: 'https://poolparty.example.org/api/'
      project-name: 'yourprojectslug'
      target-filepath: 'concepts.trig'
```


### Secret variables
This action requires two secrets to be added to the repository:
* `POOLPARTY_USERNAME`
* `POOLPARTY_PASSWORD`

These are credentials of a PoolParty API user and can be added via the repository's `Settings` --> `Secrets and Variables` --> `Actions` --> `Repository secrets` section.
