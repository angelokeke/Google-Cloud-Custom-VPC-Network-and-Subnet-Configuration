# Google Cloud: Custom VPC Network and Subnet Configuration

This project involved creating a custom-mode Virtual Private Cloud (VPC) and regional subnet in Google Cloud using Cloud Shell and the gcloud CLI. The purpose of this lab was to gain hands-on experience with cloud network provisioning, CIDR subnet allocation, and configuration validation while learning how custom VPC segmentation supports cloud security and network organization. All work was completed in a lab environment simulating how cloud engineers design and verify secure network infrastructure.

## Lab Objectives

- Activate and authenticate Google Cloud Shell
- Confirm the active project configuration
- Create a custom-mode VPC network
- Create a regional subnet with a defined CIDR range
- List and verify available networks
- Validate subnets associated with the new VPC

## Lab Environment

- Google Cloud Platform (GCP)
- Google Cloud Shell
- gcloud CLI
- Custom-mode VPC networking environment

Running the lab in Cloud Shell allowed full command-line control over network creation and auditing.

## VPC Creation and Configuration

I created a custom-mode VPC named **labnet** to allow manual subnet creation instead of automatic default subnet generation.

The terminal output confirmed:

- VPC successfully created
- Subnet mode set to **CUSTOM**

A regional subnet named **labnet-sub** was then created in the **us-east4** region with the CIDR range:

10.0.0.0/28

This subnet served as a small segmented lab network for testing and isolation.

## Network Validation and Resource Verification

To verify that the VPC was created successfully, I listed all networks in the project.

The output displayed:

- default network
- labnet network

confirming both existed in the environment.

Next, I listed subnets for the labnet network to verify:

- correct region mapping
- CIDR accuracy
- subnet association

This confirmed the subnet was properly provisioned and active inside the VPC.

## Reflection and Key Takeaways

This lab strengthened my understanding of:

- VPC design and segmentation
- CIDR subnet allocation
- regional resource mapping
- network isolation in cloud security
- validating configurations through command output

Working directly in Cloud Shell helped me build confidence reading system output and confirming successful provisioning steps. I plan to expand on this work by exploring firewall rules, routing behavior, and virtual machine deployment within segmented subnets.
