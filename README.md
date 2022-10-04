# cronjob

Dead simple CronJobs for Kubernetes.

## Example

```yaml
cronJob:
  image: registry.redhat.io/openshift4/ose-cli:v4.10
  schedule: "*/1 * * * *"
  serviceAccount: default
  script: |
    #!/bin/bash
    echo 'Hello World!'
```

## How to Use

* Fork this repo
* Replace variables in [values.yaml](values.yaml) with your own
* Deploy to your cluster with:
    * `$ helm install my-cronjob .`
