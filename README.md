# Application

Generic helm chart for applications which are:

- stateless
- create only namespace scoped resources (e.g. it doesn't need CRB - cluster role bindings)
- don't need privileged containers
- don't call the underlying Kubernetes API or use the underlying etcd as a database by defining custom resources
- run either as deployment or cronjob

## Installing the Chart

To install the chart with the release name my-application in namespace test:

    helm repo add aloprozam https://aloprozam.github.io/helm-charts
    helm repo update
    helm install my-application aloprozam/generic-app --namespace default


## Uninstall the Chart

To uninstall the chart:

    helm delete <name-of-the-chart>