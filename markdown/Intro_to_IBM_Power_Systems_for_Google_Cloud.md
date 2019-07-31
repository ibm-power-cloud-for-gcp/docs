# About IBM Power Systems for Google Cloud

IBM® Power Systems™ for Google Cloud is an infrastructure as a service solution from IBM that you can use to deploy, manage, and consume PowerVM based virtual machines (LPARs) that are connected to the Google Cloud Platform. Virtual machine (VM) management is provided by a Google aligned experience that offers APIs, command line, and web-based console options.

The IBM Power Systems for Google Cloud service is designed to deliver a public cloud-based experience with the same infrastructure capabilities that you run on premises. You can quickly deploy Power Systems VMs to meet your specific business needs. You can create a hybrid cloud environment that combines IBM Power Systems benefits and services on the Google Cloud Platform for a hybrid cloud solution.

You can use the IBM Power Systems for Google Cloud service to host virtual machines that are running the AIX operating system.

This service uses a capacity-based subscription model with monthly pricing. The subscription is based on a cloud instance plan, which is a collection of compute, memory, storage, and network resources.

## Before you subscribe

Before you subscribe to the IBM Power Systems for Google Cloud service, review the following prerequisites:

* Create a Google Cloud Project with a defined set of virtual private cloud (VPC) networks, which can be the default VPC for a project. For more information, see [Projects](https://cloud.google.com/docs/overview/#projects) and [VPC networks](https://cloud.google.com/vpc/docs/vpc).

* Identify the network IP address that you want to use for your cloud instance. Your IP address must be compatible with your existing set of Google Cloud projects and VPC networks. If you want direct connectivity between your data center and the Google Cloud Platform GCP, your IP address must work with your on-premises networks. The IP address must use the Classless Inter-Domain Routing (CIDR) notation to configure the service. This IP range must be a private IP range [RFC1918](https://tools.ietf.org/html/rfc1918) that does not overlap with any other IP ranges in your VPC or any advertised IP ranges coming from interconnects or VPNs that are used for on-prem resources. An example of an IP address that uses the CIDR notation is 172.16.1.0/24.

* Know your [IBM Customer Number (ICN)](https://www-01.ibm.com/support/docview.wss?uid=swg21507387).

## Subscribing to the service

After you select the IBM Power Systems for Google Cloud tile, review the available cloud instance plans and subscribe to the desired plan. Follow the workflow to register for the service and proceed to the initial configuration steps.

During the subscribing process, you must supply the information about your project, VPC, and the CIDR range for VMs created in your instance plan. This information is the basis of a series of gcloud commands that you run against your Google project to establish a connection to the service. This connection is a VPC Peering between your VPC and an IBM-managed tenant project over the Google network fabric. After the initial configuration is complete, access to the VM management GUI is enabled and your selected project is connected to your cloud instance. Next, you can create an LPAR and verify that you can connect to the LPAR.

You can change cloud instance plans to different size plans if capacity demands change over time.

Cloud instance plans are limited to one subscription per Google billing account.

## Service features

The following are some of the key features for the IBM Power Systems for Google Cloud service.

### Google integrated billing

Cloud plans are subscribed to from the GCP Marketplace and included in your monthly Google bill. The pricing for the Google cloud plan is based on a monthly subscription. The Google cloud plan does not have a term commitment, and you can cancel at any time. Billing is pro-rated for partial monthly usage.

### Internal Google network access to GCP resources and services

Cloud instances are networked into a target GCP project by using Google VPC Peering technology. This VPC Peering enables VMs on IBM Power System servers to obtain direct private access to GCP resources such as compute, cloud storage, and other services over the internal global Google network. You can use this connectivity for solutions spanning IBM Power Systems infrastructure and GCP resources. For more information, see [Google VPC Peering](https://cloud.google.com/vpc/docs/vpc-peering).

### Network design with a secure by default access model

VMs created on IBM Power Systems infrastructure are assigned IP addresses on the cloud instance private network within the associated GCP project. By default, IP addresses are internal to the project and only accessible from resources within the project. You have full control over network access to IBM Power Systems VMs.

You can control how the VMs are made accessible beyond their GCP project by using solutions such as front-end GCP-based application servers, VPNs, NAT gateways, jump servers for SSH access, or Google Direct Interconnect solutions to the data center.

<!--Note: I commented this out. The following figure illustrates the overall data plane design for IBM Power Systems that is connected to GCP projects and related services. __*Need to add figure*__-->

### Flexible options for managing the lifecycle of Power virtual machines and related resources

OpenAPI compliant APIs, command line, and web console options that you can use to manage the lifecycle of VMs (LPARs) from creation to deletion. Operations are also available to manage VM images, data volumes, and networks.

The command line tool is called **pcloud**. To view the documentation for the **pcloud** command, run the `pcloud docs` command. Documentation links for the API and web console are provided as part of the management web console.

### AIX license and support entitlement

The IBM Power Systems for Google Cloud service includes a license to run the AIX operating system with support entitlement for supported AIX versions. This service offers a few stock AIX images that you can deploy. You can also bring your own custom AIX images based on OVA exports from IBM Cloud PowerVC Manager. You can also use AIX `mksysb` images along with a NIM server or AIX alt disk installation to create customized LPARs within cloud instances.

### Enterprise IBM Power Systems infrastructure compatible with on-premises deployments and workloads

The IBM Power Systems for Google Cloud service is composed of IBM PowerVM based Power Systems, including the latest POWER9 technology. The infrastructure includes the following attributes:

* 16-gigabit Fibre Channel connected storage
* 25-gigabit networking for all servers
* 100-gigabit network across server racks
* HDD and SDD storage options for data volumes
* Shared and dedicated processor options when you create guest VMs
* Dynamic LPAR support for live add and remote of compute and memory to guest VMs
* PowerVM NPIV-based storage virtualization for guest VMs (LPARs)
* Dual VIOS
* Redundant SAN and network fabrics
* Redundant PDUs
* Connectivity to GCP over dual interconnect zones, each with multiple aggregated links
* PowerVC remote restart technology for improved guest VM availability with host failures
* PowerVM LPM technology to sustain guest VM availability during disruptive infrastructure maintenance events
