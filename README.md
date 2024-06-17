# Azure-week4assignment

Link for deployed webapp on azure
Link: prernatest123.azurewebsites.net

Following the assignment instructions, I successfully created a multi-tier network architecture in Azure utilizing a Hub-Spoke model. This document details the steps I took to achieve this.
Steps:

Accessed Azure Portal:

I signed in to the Azure portal.
Created Resource Group:

I created a resource group named my-student-resource-group to organize my Azure resources.

Created Virtual Network (VNet):

I created a VNet with an address space of 192.168.0.0/16.
Within the VNet, I added two subnets named subnet-1 and subnet-2 for different purposes.

Created Hub VNet (Management):

I created a separate VNet named mgmt-vnet specifically for management tasks.
Within mgmt-vnet, I created two subnets: mgmt-subnet and optional-subnet.

Created Spoke VNets (Production, Testing, Development):

I created three additional VNets for production (prod-vnet), testing (test-vnet), and development (dev-vnet) environments.
Within each spoke VNet, I created subnets for my resources: prod-subnet, test-subnet, and dev-subnet.

Configured Hub-Spoke Peering:

I established peering connections between the management VNet (mgmt-vnet) and each spoke VNet ( prod-vnet, test-vnet, and dev-vnet). This allows controlled communication between management and the different environments.
Created VMs in Each VNet:

I deployed VMs in each VNet subnet based on my specific needs (e.g., Linux/Windows VMs, SQL server).

Verified Connectivity (Ping Test):

I connected to a VM in the mgmt-subnet of the management VNet (mgmt-vnet).
Using the ping command from the management VM, I successfully tested connectivity to VMs in each spoke VNet subnet, verifying communication between the tiers.
