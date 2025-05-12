status at 2025-04, v1

# Use Cases
## End Customer
### Purchaser
- Purchase Cluster Access:
  The Purchaser logs into the cloud provider's portal, selects a cluster template, chooses a duration (e.g., 1 month), and clicks "Purchase." The system provisions access to an existing OpenShift cluster.
- Automate Cluster Scaling:
  An advanced Purchaser uses the Fulfillment API to automatically increase the number of worker nodes when their workloads require more resources, without manual intervention.
### Cluster Admin
- Prepare Cluster for Users:
  After the Purchaser obtains cluster access, the Cluster Admin logs into OpenShift, creates user namespaces, installs GPU drivers via OperatorHub, and ensures quotas are set for project isolation.
### Cluster User
- Run AI Workloads:
  A Cluster User accesses OpenShift AI tools (e.g., JupyterHub, TensorFlow serving) to train a machine learning model on an allocated project namespace, using GPUs if available.
---
## Cloud Provider
### Network Admin
- Verify Endpoint Connectivity:
  After a customer purchases cluster access, the Network Admin verifies that the reserved nodes are reachable within the internal DC network and properly segmented from other tenants.
### Server Admin
- Monitor Node Health:
  Server Admin reviews automated alerts showing disk errors on a node used by a customer cluster and initiates repair/replacement to avoid service disruption.
### OpenShift Platform Admin
- Update Management Clusters:
  Platform Admin applies updates to ACM and hosted control planes monthly, ensuring that new end customer clusters use the latest supported templates and policies.
### SREs
- Remediate Cluster Deployment Failures:
  An SRE is paged when a cluster creation workflow fails due to missing node resources. They diagnose via automation dashboards, mark bad nodes offline, and retry the cluster provisioning.
### Integration Developer
- Integrate Purchase API:
  An Integration Developer writes a Python script that connects the cloud provider's billing portal with the Fulfillment API, automating cluster provisioning immediately after a successful payment.
- Add Monitoring Hooks:
  The Integration Developer updates internal systems to monitor cluster creation events by subscribing to status changes from the Fulfillment API.
