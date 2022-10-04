# cronjob

Dead simple CronJobs for Kubernetes.

## Example

```yaml
cronJob:
  image: registry.access.redhat.com/ubi8:latest
  schedule: "*/1 * * * *"
  script: |
    #!/bin/bash
    echo 'Hello World!'
```

## How to Use

* Fork this repo (or *"Use this Template"* in GitHub)
* Replace variables in [values.yaml](values.yaml) with your own
* Deploy to your cluster with:
    * `$ helm install my-cronjob .`
* If you want the straight k8s YAML so you can manually deploy it (or view it):
    * `$ helm template --release-name my-cronjob .`
