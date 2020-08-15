# Admin Project Configuration

## Environments

* `cicd`: Environment for CI/CD tooling and builds.
* `dev`: Development environment.
* `uat`: User Acceptance Testing enviornment.

## Initial Environment Seeding

To spin up these environments without Argo CD:
```
oc apply -k environments/devops/cicd
oc apply -k environments/petclinic/dev
oc apply -k environments/petclinic/uat
```

This will setup the environments, meaning it will create:
* Namespaces
* RoleBindings
* Quotas/Limits
* NetworkPolicy

It does not spin up any actual apps or tools. That is in the `projects-team` repository.

