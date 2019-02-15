##Public Cloud Readme
Repository for Artifacts required to automate the provisioning / deprovisioning of cloud resources

**[Office365 Teams](https://teams.microsoft.com/l/team/19%3a557c18e6f3cf4b3aac7ea3a7a93dedc6%40thread.skype/conversations?groupId=df411334-0271-4029-8621-41b5921dfd6d&tenantId=b7be7686-6f97-4db7-9081-a23cf09a96b5)**
(Recommend O365 Teams for non-work item information.  Comments/questions related to work items can be attached within the work item itself.)

**[Project Glossary](https://dev.azure.com/Halliburton-IT/ITPublicCloud/_wiki/wikis/ITPublicCloud.wiki?wikiVersion=GBwikiMaster&pagePath=%2FGlossary)**

**Identity Access**

Access to MS Teams, Azure DevOps, Azure, and AWS is based on RBAC controls from the solution blueprints.  Use [Identity Self Service](http://gsaf/) to request access to the appropriate resource/role groups:

1. *Azure DevOps* - HAL_USR_ITPUBLICCLOUD_DEV (Contributors),  HAL_ADM_ITPUBLICCLOUD_DEV (Administrators)

2. *Azure* - AZ_ADM_AzDeploy_Prod_Local_Admin (Resource Contributors), GLB_ADM_Prod_ServerOperations (Server Ops Admin role), GLB_ADM_Prod_SecurityOperations (Security Ops Admin role)

**Boards**

The Boards contain Kanban boards for visualizing and managing work items.  Work Item is a generic term used for representing a unit of work.  The Work Item is further specialized into the following four (4) types:

1. *Epic* - represents a Product Release.  Each Epic/Release depends on each other for delivery.  IT + Landmark will be engaged per Epic.

2. *Feature* - represents a discrete Feature within a Release.  A Feature belongs to a specific Product Release.  A Feature can be unique to IT or Landmark.

3. *Backlog* - represents a deliverable required to complete a Feature.  A Backlog belongs to a specific Feature.  A Backlog item is generally unique to a specific group, such as IT Design Operations, IT Security, IT Architecture, Landmark DevOps, etc.

4. *Task* - represents the smallest unit of work to complete a Backlog item.  A Task belongs to a specific Backlog.  A Task is assigned to an individual.

*QuickStart: Go to 'Boards/Queries/All/All Work Items' to see a threaded view of all work items.*

**Repos**

The Repos contain the source code repository for all artifacts requiring source code management, such as Scripts.  This is a Git source control management system and can be interacted with utilizing any Git client (CLI), VSCode, Visual Studio, etc.

Source within the Repos triggers Continuous Integration (CI), aka Build/Test, and Continuous Deployment (CD) pipeline processes upon commits (check-in).

If you experience the following error when attempting to clone the repository, it is due to a missing proxy configuration for git:

*Error encountered while cloning the remote repository: Git failed with a fatal error.  unable to access 'https://dev.azure.com/Halliburton-IT/ITPublicCloud/_git/ITPublicCloud/': Failed to connect to dev.azure.com port 443: Connection refused*

To resolve, execute the following commandline to add a specific proxy server to the Git Config file:

*git config --global http.proxy np1prxy801.corp.halliburton.com:80*

You can view your Git Config settings with a list: *git config -l* 

**Pipelines**

The Pipelines contain the CI/CD automation pipeline when source/scripts are committed to the Repos.  They interact between the source repository and the target deployment system, Azure and AWS.

**Naming Conventions for Resources**

[Consolidated (Azure and AWS) naming conventions](https://teams.microsoft.com/_#/xlsx/viewer/teams/https%3A~2F~2Fhalliburton.sharepoint.com~2Fsites~2FPublicCloud~2FShared%20Documents~2FGeneral~2FNaming%20Conventions~2FITA%20Public%20Cloud%20Naming%20Conventions.xlsx)

**Architecture**

[High-Level Overview - Full Architecture](http://spwest.corp.halliburton.com/sites/ITA/ITAContents/Shared%20Documents/020100-Solutions/03-Work%20Products/Landmark%20Public%20Cloud/02-WIP/Landmark%20Public%20Cloud.pptx?web=1)

1. [Release 1 Overview - Basic Disconnected Tenant](http://spwest.corp.halliburton.com/sites/ITA/ITAContents/Shared%20Documents/020100-Solutions/03-Work%20Products/Landmark%20Public%20Cloud/02-WIP/Public%20Cloud%20Basic%20Tenant%20-%20Release%201.pptx?web=1)

2. [Release 2 Overview - Advanced Networking](http://spwest.corp.halliburton.com/sites/ITA/ITAContents/Shared%20Documents/020100-Solutions/03-Work%20Products/Landmark%20Public%20Cloud/02-WIP/Public%20Cloud%20Advanced%20Networking%20-%20Release%202.pptx?web=1)

3. [Release 3 Overview - Secure Workloads](http://spwest/sites/ITA/ITAContents/Shared%20Documents/020100-Solutions/03-Work%20Products/Landmark%20Public%20Cloud/02-WIP/Public%20Cloud%20Secure%20Workloads%20-%20Release%203.pptx)

4. [Release 4 Overview - MVP for Customer Production](http://spwest/sites/ITA/ITAContents/Shared%20Documents/020100-Solutions/03-Work%20Products/Landmark%20Public%20Cloud/02-WIP/Public%20Cloud%20MVP%20for%20Customer%20Production%20-%20Release%204.pptx?web=1)

5. [Release 5 Overview - Operational Efficiency](http://spwest/sites/ITA/ITAContents/Shared%20Documents/020100-Solutions/03-Work%20Products/Landmark%20Public%20Cloud/02-WIP/Public%20Cloud%20Operational%20Efficiency%20-%20Release%205.pptx?web=1)

[Azure AD Solution Blueprint](http://spwest.corp.halliburton.com/sites/ITA/ITAContents/Shared%20Documents/020100-Solutions/03-Work%20Products/Azure%20AD/01-Published/ITA%20Azure%20AD%20SBP.pdf)

[Azure Solution Blueprint](http://spwest/sites/ITA/ITAContents/Shared%20Documents/020100-Solutions/03-Work%20Products/Azure%20Solution%20Blueprint/02-WIP/ITA%20Azure%20SBP.docx)

[AWS Solution Blueprint](http://spwest/sites/ITA/ITAContents/Shared%20Documents/020100-Solutions/03-Work%20Products/AWS%20Cloud/02-WIP/ITA%20AWS%20SBP.docx)

[Okta Solution Blueprint](http://spwest.corp.halliburton.com/sites/ITA/ITAContents/Shared%20Documents/020100-Solutions/03-Work%20Products/Okta/01-Published/ITA%20Okta%20SBP.pdf)

[RBAC Solution Blueprint](http://spwest.corp.halliburton.com/sites/ITA/ITAContents/Shared%20Documents/020100-Solutions/03-Work%20Products/RBAC%20Groups/01-Published/ITA%20RBAC%20Groups%20SBP.pdf)

[Role Delegation for Policy Management, Provisioning, Configuration](http://spwest.corp.halliburton.com/sites/ITA/ITAContents/Shared%20Documents/020100-Solutions/03-Work%20Products/Landmark%20Public%20Cloud/02-WIP/Public%20Cloud%20Role%20Delegation%20for%20Policy%20Provisioning%20Configuration.pptx)

**Azure Resources**

[Best Practices For Using Azure Resource Manager Templates](https://blogs.msdn.microsoft.com/mvpawardprogram/2018/05/01/azure-resource-manager/)

**AWS Resources**

