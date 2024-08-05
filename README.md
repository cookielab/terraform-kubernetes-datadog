# Terraform module for Kubernetes Datadog

> [!WARNING]  
> This module is no longer maintained. We recommend switching to [Helm](https://artifacthub.io/packages/helm/datadog/datadog).

This module deploys [Datadog](https://docs.datadoghq.com/agent/kubernetes/daemonset_setup/) to your Kubernetes cluster.

## Usage

```terraform
provider "kubernetes" {
  # your kubernetes provider config
}

module "datadog" {
  source = "cookielab/datadog/kubernetes"
  version = "0.9.0"

  datadog_agent_api_key = "<YOUR_API_KEY>"
  datadog_agent_site = "datadoghq.com" # Set to "datadoghq.eu" to send your Agent data to the Datadog EU site (default: "datadoghq.com")
}
```
