# Kubernetes Manifests for Jenkins Deployment

These files need to be applied in this order:

1. namespace.yaml
2. serviceAccount.yaml
3. pvc.yaml
4. deployment.yaml
5. service.yaml

* Get the initial admin password from the jenkins pod log created by the deployment.
* Remove unneeded plugins and let the rest install.
* Install the Kubernetes plugin.
* Create a Kubernetes cloud
    * Configure the namespace as `devops-tools`
    * Update the JENKINS_TUNNEL to http://\<cluster-ip\>:50000
