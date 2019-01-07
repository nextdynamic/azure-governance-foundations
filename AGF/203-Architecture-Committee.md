Architecture Committee
======================

### This document is still under development. 

### Please check back later.

Templates and DevOps
====================

As highlighted in the Automate section, your goal as an organization should be
to provision resources through source-controlled templates and scripts and to
minimize interactive configuration of your environments. This approach of
"infrastructure as code" along with a disciplined DevOps process for continuous
deployment can ensure consistency and reduce drift across your environments.
Almost every Azure resource is deployable through [Azure Resource Manager (ARM)
JSON
templates](https://github.com/rdendtler/architecture-center/blob/eca/scaffold-v2/azure/azure-resource-manager/resource-group-template-deploy)
in conjunction with PowerShell or the Azure cross platform CLI and tools such as
Terraform from Hashicorp (which has first class support and integrated into the
Azure Cloud Shell).

Article such as [this
one](https://blogs.msdn.microsoft.com/mvpawardprogram/2018/05/01/azure-resource-manager/)
provide an excellent discussion on best practices and lessons learned in
applying a DevOps approach to ARM templates with the [Azure
DevOps](https://github.com/rdendtler/architecture-center/blob/eca/scaffold-v2/azure/devops/user-guide/?view=vsts)
tool chain. Take the time and effort to develop a core set of templates specific
to your organization's requirements, and to develop continuous delivery
pipelines with DevOps tool chains (Azure DevOps, Jenkins, Bamboo, Teamcity,
Concourse), especially for your production and QA environments. There is a large
library of [Azure Quick Start
templates](https://github.com/Azure/azure-quickstart-templates) on GitHub that
you can use as a starting point for templates, and you can quickly create
cloud-based delivery pipelines with Azure DevOps.

As a best practice for production subscriptions or resource groups, your goal
should be utilizing RBAC security to disallow interactive users by default and
utilizing automated continuous delivery pipelines based on service principals to
provision all resources and deliver all application code. No admin or developer
should touch the Azure Portal to interactively configure resources. This level
of DevOps takes a concerted effort and utilizes all the concepts of the Azure
scaffold and provides a consistent and more secure environment that will meet
your organizations to grow scale.

[!TIP] When designing and developing complex ARM templates, use [linked
templates](https://github.com/rdendtler/architecture-center/blob/eca/scaffold-v2/azure/azure-resource-manager/resource-group-linked-templates)
to organize and refactor complex resource relationships from monolithic JSON
files. This will enable you to manage resources individually and make your
templates more readable, testable and reusable.

Azure is a hyper scale cloud provider and as you move your organization from the
world of on-premises servers to the cloud, utilizing the same concepts that
cloud providers and SaaS applications use will provide your organization to
react to the needs of the business in vastly more efficient way.
