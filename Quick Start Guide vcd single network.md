# About This Guide

This quick start guide is intended to help you rapidly deploy PrimaryIO HDM to a test environment. The steps are intended for a single on-premises network environment, with cloud access via a WAN link and no separation of the management and VM network. All IP assignments in this guide are static/static-pool and connectivity between the on-premises and cloud environments is via IPSec. For other types of network configurations, refer to the HDM 2.1 Install Guide.

HDM provides a flexible deployment model to cater to a wide range of user needs, including different use cases, performance requirements, scalability, and levels of security. The HDM 2.1 Install Guide contains full details of every deployment mode. For simplicity, this document describes an HDM deployment using the Standalone, Ultra-Lite option. This option supports all the key features of HDM and can also be used for cold migration and validation purposes.

The following steps are required to deploy HDM:

1. Review System Requirements (estimated time: 15 minutes)
1. Download PrimaryIO HDM (estimated time: 5 minutes – depending on Internet speed)
1. Network Planning & Mapping (estimated time: 20 minutes)
1. Deploy the HDM Appliance (estimated time: 5 minutes)
1. Validate the Network Configuration (estimated time: 5 minutes)
1. On-premises Deployment (estimated time: 10 minutes)
1. Cloud Deployment (estimated time: 45-60 minutes)
1. Perform a Cold Migration (estimated time: dependent on VM size)

# Step 1: Review System Requirements

Refer to the System Requirements in Appendix A of this document. Printing a copy of Appendix A to use as a checklist is recommended.

# Step 2: Download PrimaryIO HDM
To obtain your license and download link for HDM, visit https://www.primaryio.com/ibm/

 

You will receive an email with the following:

* A link to download the PrimaryIO HDM software
* A link to training videos
* A license key for the software
 

Before proceeding with the installation, watch the training videos and use this guide.


# Step 3: Network Planning and Mapping
Network configuration information is required at key points throughout the deployment process. So, develop a network connectivity plan prior to deploying HDM. This section will help guide you through that process. The information captured in this section will be employed later in the installation process. If an IPSec tunnel and cloud configuration have not yet been established, these must be done before moving any further. Follow the steps outlined in Appendix C of this document. Please be aware that this process will add 30 minutes to the estimated time to complete this section.

Once connectivity and cloud configuration are complete, be sure to record all applicable details in Appendix B of this document for easy reference later in the deployment process.

The following is required to complete the network plan:

1. IPSec tunnel, firewall, and cloud network configuration information (See Appendix C)
1. Network requirements during OVF deployment
1. Network requirements during on-premises deployment
1. Network requirements during cloud deployment

# Choose or Create an appropriate network:

A simple network configuration where all connectivity to the cloud is available through one network (e.g., hdm_network). Here hdm_network should have access to the following:

* On-premises vCenter
* Cloud vCenter via WAN link
* On-premises ESXi
* Cloud ESXi
* HDM Appliance

The required connectivity is highlighted in figure 1. For all steps in the deployment that require a VMware network as input, provide the identified or created hdm_network. It will also be necessary to create two networks in the cloud, hdm_routed_network and hdm_internal.

