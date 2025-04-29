# Windows Demos

## Table of Contents
- [Windows Demos](#windows-demos)
  - [Table of Contents](#table-of-contents)
  - [About These Demos](#about-these-demos)
    - [Known Issues](#known-issues)
    - [Jobs](#jobs)
    - [Workflows](#workflows)
  - [Suggested Usage](#suggested-usage)

## About These Demos
This category of demos shows examples of Windows Server operations and management with Ansible Automation Platform. The list of demos can be found below. See the [Suggested Usage](#suggested-usage) section of this document for recommendations on how to best use these demos.

### Known Issues
We are currently investigating an intermittent connectivity issue related to the credentials for Windows hosts. If encountered, re-provision your demo environment. You can track the issue and related work [here](https://github.com/ansible/product-demos/issues/176).

### Jobs

- [**Windows / Install IIS**](install_iis.yml) - Install IIS feature with a configurable index.html
- [**Windows / Patching**](patching.yml) - Apply Windows updates by category and create report
- [**Windows / Arbitrary Powershell**](arbitrary_powershell.yml) - Run given Powershell script (default: retrieve cat fact from API)
- [**Windows / Powershell Script**](powershell_script.yml) - Run a Powershell script stored in source control to query services
- [**Windows / Powershell DSC configuring password requirements**](powershell_dsc.yml) - Configure password complexity with Powershell desired state config
- [**Windows / Create Active Directory Domain**](create_ad_domain.yml) - Create a new AD Domain
- [**Windows / Helpdesk new user portal**](helpdesk_new_user_portal.yml) - Create user in AD Domain
- [**Windows / Join Active Directory Domain**](join_ad_domain.yml) - Join computer to AD Domain

### Workflows
- [**Setup Active Directory Domain**](setup_domain_workflow.md) - A workflow to create a domain controller with two domain-joined Windows hosts

## Suggested Usage

**Setup Active Directory Domain** - One-click domain setup, infrastructure included.

**Windows / Create Active Directory Domain** - This job can take some to complete. It is recommended to run ahead of time if you would like to demo creating a helpdesk user.

**Windows / Helpdesk new user portal** - This job is dependant on the Create Active Directory Domain completing before users can be created.

**Windows / Join Active Directory Domain** - This job is dependant on the Create Active Directory Domain completing before computers can be joined.