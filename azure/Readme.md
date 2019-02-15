###Azure Public Cloud Readme
Repository for Artifacts required to automate provisioning / deprovisioning of Azure cloud resources.
The projects are utilizing a Nested ARM template deployment pattern where each project contains a template.  Root templates are utilized for a use-case deployment linking the generic templates during provisioning.

##How to Run:

Step 1: Run the Root template project for - example: hal.azure.basictenant (use artifacts storage from Step 1)

##Project Structure:
1) hal.azure.basictenant

   Root template for deploying a Basic Tenant configuration

2) hal.azure.template.vnet

   VNET template

3) hal.azure.template.keyvault

   Keyvault template