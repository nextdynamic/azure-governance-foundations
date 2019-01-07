Automation Committee
====================

### This document is still under development. 

### Please check back later.

### Ruthless Automation

One of the many capabilities that differentiates the maturity of organizations
using cloud providers is the level of automation that they have incorporated.
Automation is a never-ending process and as your organization moves to the cloud
it is any area that you need to invest resources and time in building.
Automation serves many purposes including consistent rollout of resources (where
it ties directly to another core scaffold concept, Templates & DevOps) to the
remediation of issues. Automation is the "connective tissue" of the Azure
scaffold and links each area together.

There are a number of tools that are available as you build out this capability,
from first party tools such as Azure Automation, EventGrid and AzureCLI to an
extensive amount of third party tools such as Terraform, Jenkins, Chef, and
Puppet (to name a few). Core to your operations team ability to automate are
Azure Automation, Event Grid and the Azure Cloud Shell:

-   **Azure Automation**: Is a cloud-based capability that allows to you author
    Runbooks (in either PowerShell or Python) and allows you automate processes,
    configure resources, and even apply patches. [Azure
    Automation](https://github.com/rdendtler/architecture-center/blob/eca/scaffold-v2/azure/automation/automation-intro)
    has an extensive set of cross platform capabilities that are integral to
    your deployment but are too extensive to be covered in depth here.

-   **Event Grid**: this
    [service](https://github.com/rdendtler/architecture-center/blob/eca/scaffold-v2/azure/event-grid)
    is a fully-managed event routing system that let's you react to events
    within your Azure environment. Like Automation is the connective tissue of
    mature cloud organizations, Event Grid is the connective tissue of good
    automation. Using Event Grid, you can create a simple, serverless, action to
    send an email to an administrator whenever a new resource is created and log
    that resource in a database. That same Event Grid can notify when a resource
    is deleted and remove the item from the database.

-   **Azure Cloud Shell**: is an interactive, browser-based
    [shell](https://github.com/rdendtler/architecture-center/blob/eca/scaffold-v2/azure/cloud-shell/overview)
    for managing resources in Azure. It provides a complete environment for
    either PowerShell or Bash that is launched as needed (and maintained for
    you) so that you have a consistent environment from which to run your
    scripts. The Azure Cloud Shell provides access to additional key tools
    -already installed-- to automate your environment including [Azure
    CLI](https://github.com/rdendtler/architecture-center/blob/eca/scaffold-v2/cli/azure/get-started-with-azure-cli?view=azure-cli-latest),
    [Terraform](https://github.com/rdendtler/architecture-center/blob/eca/scaffold-v2/azure/virtual-machines/linux/terraform-install-configure)
    and a growing list of additional
    [tools](https://azure.microsoft.com/updates/cloud-shell-new-cli-tools-and-font-size-selection/)
    to manage containers, databases (sqlcmd) and more.

Automation is a full-time job and it will rapidly become one of the most
important operational tasks within your cloud team. Organizations that take the
approach of "automate first" have greater success in using Azure:

-   Managing costs: actively seeking opportunities and creating automation to
    re-size resources, scale-up/down and turn off unused resources.

-   Operational flexibility: through the use of automation (along with Templates
    and DevOps) you gain a level of repeatability that increases availability,
    increases security and enables your team to focus on solving business
    problems.

Azure Update Management
-----------------------

One of the key tasks you can do to keep your environment safe is ensure that
your servers are patched with the latest updates. While there are many tools to
accomplish this, Azure provides the [Azure Update
Management](https://github.com/rdendtler/architecture-center/blob/eca/scaffold-v2/azure/automation/automation-update-management)
solution to address the identification and rollout of critical OS patches. It
makes use of Azure Automation (which is covered in the
[Automate](https://github.com/rdendtler/architecture-center/blob/eca/scaffold-v2/docs/cloud-adoption/appendix/azure-scaffold.md#automate)
section, later in this guide.
