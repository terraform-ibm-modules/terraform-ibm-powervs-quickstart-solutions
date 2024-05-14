<!-- Update this title with a descriptive name. Use sentence case. -->
# Terraform modules template project

<!--
Update status and "latest release" badges:
  1. For the status options, see https://terraform-ibm-modules.github.io/documentation/#/badge-status
  2. Update the "latest release" badge to point to the correct module's repo. Replace "terraform-ibm-module-template" in two places.
-->
[![Incubating (Not yet consumable)](https://img.shields.io/badge/status-Incubating%20(Not%20yet%20consumable)-red)](https://terraform-ibm-modules.github.io/documentation/#/badge-status)
[![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit&logoColor=white)](https://github.com/pre-commit/pre-commit)
[![Renovate enabled](https://img.shields.io/badge/renovate-enabled-brightgreen.svg)](https://renovatebot.com/)
[![semantic-release](https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg)](https://github.com/semantic-release/semantic-release)

## Summary
This repository contains deployable architecture solutions that help provision PowerVS Instances Quickly. The solutions are available in the IBM Cloud Catalog and can also be deployed without the catalog as well..

Solutions offered:
1. [PowerVS Instance variation](https://github.com/terraform-ibm-modules/terraform-ibm-powervs-quickstart-solutions/tree/main/solutions/powervsi-with-vpc-landing-zone)
    - Creates a VPC and a Power Virtual Server workspace, interconnects them, and configures operating network management services (SQUID proxy, NTP, NFS, and DNS services) using Ansible Galaxy collection roles [ibm.power_linux_sap collection](https://galaxy.ansible.com/ui/repo/published/ibm/power_linux_sap/).
    - Additionally creates a Power Virtual Server Instance of a selected t-shirt size.
    - This solution is typically utilized for **PoCs, demos, and quick onboarding** to PowerVS Infrastructure.

## Reference architectures
- [PowerVS Instance Variation]https://github.com/terraform-ibm-modules/terraform-ibm-powervs-quickstart-solutions/blob/main/reference-architectures/powervsi-with-vpc-landing-zone/deploy-arch-ibm-powervsi-with-vpc-landing-zone.svg)

## Solutions
| Variation  | Available on IBM Catalog  |  Requires IBM Schematics Workspace ID | Creates VPC Landing Zone | Performs VPC VSI OS Config | Creates PowerVS Infrastructure | Creates PowerVS Instance | Performs PowerVS OS Config |
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
| [PowerVS Instance](https://github.com/terraform-ibm-modules/terraform-ibm-powervs-infrastructure/tree/main/solutions/quickstart)    | :heavy_check_mark:  |   N/A  | :heavy_check_mark:| :heavy_check_mark: | :heavy_check_mark:  | :heavy_check_mark: | N/A |

<!-- BEGIN OVERVIEW HOOK -->
## Overview
* [terraform-ibm-powervs-quickstart-solutions](#terraform-ibm-powervs-quickstart-solutions)
* [Contributing](#contributing)
<!-- END OVERVIEW HOOK -->


## Required IAM access policies

You need the following permissions to run this module.

- Account Management
    - **Resource Group** service
        - `Viewer` platform access
    - IAM Services
        - **Workspace for Power Virtual Server** service
        - **Power Virtual Server** service
            - `Editor` platform access
        - **VPC Infrastructure Services** service
            - `Editor` platform access
        - **Transit Gateway** service
            - `Editor` platform access
        - **Direct Link** service
            - `Editor` platform access

<!-- END MODULE HOOK -->


<!-- BEGIN CONTRIBUTING HOOK -->
## Contributing

You can report issues and request features for this module in GitHub issues in the module repository. See [Report an issue or request a feature](https://github.com/terraform-ibm-modules/.github/blob/main/.github/SUPPORT.md).

To set up your local development environment, see [Local development setup](https://terraform-ibm-modules.github.io/documentation/#/local-dev-setup) in the project documentation.
<!-- END CONTRIBUTING HOOK -->
