---
title: Microsoft Azure Data Box Disk system requirements| Microsoft Docs
description: Learn about the software and networking requirements for your Azure Data Box Disk 
services: databox
author: stevenmatthew

ms.service: databox
ms.subservice: disk
ms.topic: article
ms.date: 10/11/2022
ms.author: shaas
---

::: zone target="docs"

# Azure Data Box Disk system requirements

> [!CAUTION]
> This article references CentOS, a Linux distribution that is nearing End Of Life (EOL) status. Please consider your use and planning accordingly. For more information, see the [CentOS End Of Life guidance](~/articles/virtual-machines/workloads/centos/centos-end-of-life.md).

This article describes the important system requirements for your Microsoft Azure Data Box Disk solution and for the clients connecting to the Data Box Disk. We recommend that you review the information carefully before you deploy your Data Box Disk, and then refer back to it as necessary during the deployment and subsequent operation.

The system requirements include the supported platforms for clients connecting to disks, supported storage accounts, and storage types.

::: zone-end

::: zone target="chromeless"

## Review prerequisites

1. You must have ordered your Data Box Disk using the [Tutorial: Order your Azure Data Box Disk](data-box-disk-deploy-ordered.md). You have received your disks and one connecting cable per disk.
2. You have a client computer available from which you can copy the data. Your client computer must:

    - Run a supported operating system.
    - Have other required software installed.

::: zone-end

## Supported operating systems for clients

Here is a list of the supported operating systems for the disk unlock and data copy operation via the clients connected to the Data Box Disk.

| **Operating system** | **Tested versions** |
| --- | --- |
| Windows Server |2008 R2 SP1 <br> 2012 <br> 2012 R2 <br> 2016 |
| Windows (64-bit) |7, 8, 10, 11 |
|Linux <br> <li> Ubuntu </li><li> Debian </li><li> Red Hat Enterprise Linux (RHEL) </li><li> CentOS| <br>14.04, 16.04, 18.04 <br> 8.11, 9 <br> 7.0 <br> 6.5, 6.9, 7.0, 7.5 |  

## Other required software for Windows clients

For Windows client, following should also be installed.

| **Software**| **Version** |
| --- | --- |
| Windows PowerShell |5.0 |
| .NET Framework |4.5.1 |
| Windows Management Framework |5.1|
| BitLocker| - |

## Other required software for Linux clients

For Linux client, the Data Box Disk toolset installs the following required software:

- dislocker
- OpenSSL

## Supported connection

The client computer containing the data must have a USB 3.0 or later port. The disks connect to this client using the provided cable.

## Supported storage accounts

> [!Note]
> Classic storage accounts will not be supported starting **August 1, 2023**.

Here is a list of the supported storage types for the Data Box Disk.

| **Storage account** | **Supported access tiers** |
| --- | --- |
| Classic Standard | |
| General-purpose v1 Standard  | Hot, Cool |
| General-purpose v1 Premium   |  |
| General-purpose v2 Standard<sup>*</sup> | Hot, Cool |
| General-purpose v2 Premium   |  |
| Blob storage account | |
| Block Blob storage Premium | |

<sup>*</sup> *Azure Data Lake Storage Gen2 (ADLS Gen2) is supported.*

> [!IMPORTANT]
> Network File System (NFS) 3.0 protocol support in Azure Blob storage is not supported with Data Box Disk.

## Supported storage types for upload

Here is a list of the storage types supported for uploaded to Azure using Data Box Disk.

| **File format** | **Notes** |
| --- | --- |
| Azure block blob | |
| Azure page blob  | |
| Azure Files  | |
| Managed Disks | |

::: zone target="docs"

## Next step

* [Deploy your Azure Data Box Disk](data-box-disk-deploy-ordered.md)

::: zone-end

