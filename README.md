# Azure Hyper-V Lab

Hey everyone 👋

This Template will automate the deployment of an Azure IaaS VM running Windows Server 2022 OS, having Hyper-V Role enabled. By this, you will be able to experiment with Hyper-V, learn, build a proof of concept or non-production environments or even use it as staging environment for creating custom images that will be used on public Azure.

The Template consists of the following resources:

+ A Virtual Network(VNet) with 1 Subnet
+ A Standard SKU Static Public IP
+ A Network Security Group (NSG) configured to allow Remote Desktop Connections
+ A Virtual Machine that is capable of Nested Virtualization - 
+ Two Premium SSD Disks - One for Operating System(127GB) and One for Storing Virtual Machines(512GB)

Server Roles:

+ Hyper-V
+ DHCP Server
+ RSAT Tools
+ Containers

Additional Software Included with the VM:

+ Azure Az PowerShell module
+ Azure CLI
+ Azure Storage Explorer
+ AzCopy Utility
+ PowerShell Core
+ Windows Admin Center
+ 7-Zip
+ Chocolatey Package Manager

[![Visualize](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/visualizebutton.svg?sanitize=true)](http://armviz.io/#/?load=https%3A%2F%2Fraw.githubusercontent.com%2Fgeorge-markou%2FAzure-Hyper-V-Lab%2Fmain%2Fmain.json)

## Get Started

1. Press the button below to deploy the Template using the Azure Portal.

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fgeorge-markou%2FAzure-Hyper-V-Lab%2Fmain%2Fmain.json)

2. Fill in the required information.

![](./images/template.png)

3. Enjoy a cup of coffee :coffee: while waiting for the deployment to finish(Approx 15m).

![](./images/deployment.png)

4. Connect to the newly deployed VM using Remote Desktop.

![](./images/connection.png)

5. Start Managing Hyper-V either using Hyper-V Manager or Windows Admin Center.

![](./images/shortcuts.png)

## General Notes

+ There is a large list of VM sizes specified as allowed values within the Template. Just to make your life easier and avoid deployment errors :superhero:.
+ To evaluate Microsoft Software and Operating Systems, use the Desktop Shortcut of the Microsoft Evaluation Center.
+ The default path for storing Virtual Machine configuration files is "F:\VMS" and for disks is "F:\VMS\Disks".
+ Enhanced Session Mode is set to Enabled.
+ A DHCP Scope is present, providing Network Addressing to Virtual Machines.
+ An Internal Hyper-V Switch that is Nat enabled is present.
+ The Data Disk (Volume F) is formatted with ReFS and unit size 64KB.
+ You will find both JSON and Bicep Templates within this repo.
+ The DSC Configuration File is listed here [here](dsc/DSCInstallWindowsFeatures.ps1).
+ The Host Configuration File is listed here [here](/HostConfig.ps1).

## Learn more about Hyper-V

+ Windows Server Hyper-V and Virtualization Learning Path on [Microsoft Learn](https://docs.microsoft.com/en-us/learn/paths/windows-server-hyper-v-virtualization/)
+ Virtualization [Blog](https://techcommunity.microsoft.com/t5/virtualization/bg-p/Virtualization)
+ MSLab [GitHub Project](https://github.com/microsoft/MSLab)
