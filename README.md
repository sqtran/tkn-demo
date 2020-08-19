# tkn-demo
Openshift Pipeline Demo

This is a demo of Openshift Pipelines, which uses Tekton under the hood.

Right now it only has an s2i Task, which required some shortcuts to get working.

Demo TODOs
- Set up CA Cert so we don't need to disable SSL Verification
- Create tasks for individual maven build, test, and scan(s)

To get started, you'll need to be logged into a Kubernetes cluster.

```bash
oc apply -f manifests/spring-boot-image.yaml
oc apply -f manifests/spring-boot-repo.yaml
oc apply -f manifests/s2i-pipeline.yaml
```