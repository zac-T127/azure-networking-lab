# azure-networking-lab

Deployment and configuration of a Microsoft Azure network environment

## Project Overview

The goal of this project is to gain a deeper understanding of Azure through practical methods, a segmented Azure network that contains multiple subnets for public and internal services will be created.

The network will then be configured with security controls while virtual machines will be deployed to test connectivity between the resources. The valid connection will then be deliberately altered to create a scenario that requires troubleshooting. This scenario will provide a practical understanding of the Azure cloud environment. 

## Network Design

| Resource | Address Range | Purpose |
|---|---|---|
| Vnet | 10.0.0.0/16 | Create a virtual network
| Web Subnet | 10.0.1.0/24 | Create a subnet for public facing services
| Internal Subnet | 10.0.2.0/24 | Create a subnet for private services

## Design Decisions

A /16 design for Vnet was chosen to allow for plenty of room for subnets as the environment expands.

A /24 was picked for both subnets to provide 256 addresses per subnet while keeping internal and web services separated. Separating these services gives the option to apply different network security rules for public and private resources.
