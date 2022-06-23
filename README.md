## Automate terraform modules versioning with GitHub actions

While working with Terraform modules it usually happens that after committing the code you have to do several actions that needed to be executed for a complete modification of a Terraform module. Those actions are like:

- updating the documentation
- finding out next semver for the module
- tagging the module ( or creating a release )

This work flow will help to automate above tasks with several actions.

pr-checks.yml will run checks for label foreach PR action
tf-module-actions.yml is checking for TFsec vulnerabilities and also generating Terraform module documentation on every change
tf-module-release.yml will add new tags after few checks.

Assign the variables correct value while integrating it to a terraform project.