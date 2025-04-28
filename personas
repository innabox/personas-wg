status at 2025-04, v1

# Personas
## End Customer
### Purchaser
- Needed in POC1+.
- Purchases access to a cluster for a period of time.
- Uses the cloud provider’s website as the primary interface.
- May automate creation, deletion, and scaling of clusters via APIs as an advanced user.
### Cluster Admin
- Needed in POC2+.
- Makes cluster access available to users, possibly limited by namespace or using existing OpenShift capabilities.
- Installs drivers and cluster-wide software, such as operators.
- Responsible for upgrading the cluster over time.
- Might also be the Purchaser and Cluster User.
### Cluster User
- Needed in POC1+.
- Utilizes a cluster with OpenShift AI to accomplish AI tasks.
- Might also be the Purchaser.
---
## Cloud provider
### Network Admin
- Needed in POC?.
- Owns and manages the Data Center (DC) network.
- Maintains an inventory source of truth, including connectivity to endpoints.
- Might not prefer delegating management of part of their network to our automation and associated dynamic network configuration.
  - Cluster network admin
  - Node network admin
### Server Admin
- Needed in POC?.
- Owns the DC hardware.
- Monitors hardware health and facilitates repair or replacement.
- Maintains an inventory source of truth.
### OpenShift Platform Admin
- Needed in POC?.
- Owns and manages any management clusters, including those running ACM and hosted control planes.
- Responsible for automation that configures end customer clusters and associated policies.
### SREs
- Needed in POC?.
- Keep the management clusters running.
- Maintain the automation associated with cluster creation, deletion, scaling, and other operations.
- Monitor the health of end customer clusters and remediate as appropriate (need to scope this to what’s appropriate for them to access or not about a cluster’s activity).

### Integration Developer
- Needed in POC?.
- Responsible for integrating the cloud provider’s systems with the APIs provided by our systems, primarily the Fulfillment API.
- Proficient with a programming language such as Python, Go, or Java, and experienced in API integration.
- Understands how to use the APIs to implement functional (e.g., creating a cluster) and non-functional requirements (e.g., communication, authentication, performance).
- Requires access to appropriate technical means to use the APIs.
- Should be supported with reference documentation of the API (e.g., gRPC or OpenAPI specifications) and examples.
- Ideally, SDKs in Python, Go, and Java should be provided to simplify API usage (libraries in Python, Go, and Java).
