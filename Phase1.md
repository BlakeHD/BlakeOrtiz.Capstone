

# Phase 1 – Environment & Baseline
# Introduction

## Purpose

The purpose of Phase 1 is to build, configure, and validate a stable enterprise environment that will be used throughout the Migration & Stabilization capstone project. This environment serves as the foundation for all future migration, troubleshooting, stabilization, and validation activities.

Throughout this phase, I am responsible for deploying the required virtual machines, configuring the network environment, establishing Active Directory services, implementing baseline file-sharing services, and validating that all required systems are functioning correctly.

##  Goals

By the completion of this phase, my environment must provide:

* A functional Windows domain
* Centralized authentication
* Domain users and groups
* A domain-joined Windows client
* Network connectivity between systems
* A functioning file share
* A validated baseline suitable for future migration activities

---

# Environment Preparation

## Virtualization Platform

The environment was built using Oracle VirtualBox.

### Hypervisor Configuration

| Component                | Value      |
| ------------------------ | ---------- |
| Hypervisor               | VirtualBox |
| Extension Pack Installed | Yes        |
| Virtualization Enabled   | Yes        |
| Clipboard Integration    | Enabled    |

### Verification Steps

Before creating any virtual machines, I verified:

* Virtualization was enabled in BIOS/UEFI
* VirtualBox was installed successfully
* VirtualBox Extension Pack was installed
* Bidirectional clipboard functionality was operational

### Screenshot 


### Notes

> Add installation notes, version numbers, or observations here.

---

# Virtual Machine Creation

First, I setup the windows server VM with the following settings. 

## Windows Server Virtual Machine Configuration

| Setting          | Value               |
| ---------------- | ------------------- |
| VM Name          | MIG-SRV01           |
| Operating System | Windows Server 2022 |
| CPU              | 2 Cores             |
| Memory           | 6 GB                |
| Storage          | 40 GB               |
| Network Adapter  | Internal Network    |

### Screenshot 


###  Notes

> Documenteed the VM creation process and any observations.

---

## Windows 11 Client Virtual Machine Configuration

| Setting          | Value            |
| ---------------- | ---------------- |
| VM Name          | MIG-CLI01        |
| Operating System | Windows 11       |
| CPU              | 2 Cores          |
| Memory           | 4 GB             |
| Storage          | 60 GB            |
| Network Adapter  | Internal Network |

### Screenshot 


### Notes

> 
---

## Network Configuration
---

Both virtual machines were connected to the same Internal Network to allow communication without exposing the environment externally.

### Screenshot 

![ Placeholder](../screenshots/phase1/network-configuration.png)

### Notes

> * Make Sure "Promiscuous Mode" has the Option "Allow VMs" selected. This will allow our VMs too talk to one another on the virtual network. While proibiting communication to our host machine.. 


---

# Operating System Installation

## Windows Server 2022 Installation

I installed Windows Server 2022 and completed the initial operating system setup.

### Screenshot 

![ Placeholder](../screenshots/phase1/windows-server-installation.png)

### Installation Notes

> Document installation steps and observations.

---

## Windows 11 Installation

I installed Windows 11 and completed the initial workstation setup.

### Screenshot

![ Placeholder](../screenshots/phase1/windows11-installation.png)

###  Notes

> Document installation steps and observations.

---

# Initial System State Validation

Before applying any enterprise configuration, I verified that both systems met the required pre-configuration state.

## Windows Server Validation Checklist

* [ ] Clean operating system installation
* [ ] Logged in as local Administrator
* [ ] No server roles installed
* [ ] Not joined to a domain
* [ ] No enterprise configuration applied

### Screenshot 

![ Placeholder](../screenshots/phase1/server-preconfiguration-state.png)

---

## Windows Client Validation Checklist

* [ ] Clean operating system installation
* [ ] Logged in with local account
* [ ] Not joined to a domain

### Screenshot 

![ Placeholder](../screenshots/phase1/client-preconfiguration-state.png)

---

# Domain Environment Configuration

## Domain Configuration

### Domain Information

| Setting      | Value           |
| ------------ | --------------- |
| Domain Name  | migration.local |
| NetBIOS Name | MIGRATION       |

### Screenshot 

![ Placeholder](../screenshots/phase1/domain-creation.png)

### Notes

> Document domain creation process.

---

## Active Directory Configuration

I installed and configured Active Directory Domain Services to provide centralized authentication and management.

### Screenshot 

![ Placeholder](../screenshots/phase1/active-directory-configuration.png)

### Notes

> Document AD DS configuration.

---

## DNS Configuration

I configured DNS services to support name resolution within the environment.

### Screenshot 

![ Placeholder](../screenshots/phase1/dns-configuration.png)

### Notes

> Document DNS configuration details.

---

## User Account Creation

### Domain Administrator

| Account        | Purpose                |
| -------------- | ---------------------- |
| MigrationAdmin | Administrative Account |

### Standard User

| Account       | Purpose              |
| ------------- | -------------------- |
| MigrationUser | Standard Domain User |

### Screenshot Placeholder

![Screenshot Placeholder](../screenshots/phase1/user-account-creation.png)

---

## Group Creation

### Security Groups

| Group Name     | Purpose                |
| -------------- | ---------------------- |
| IT-Admins      | Administrative Access  |
| Domain-Users   | Standard User Access   |
| FileShareUsers | File Share Permissions |

### Screenshot Placeholder

![Screenshot Placeholder](../screenshots/phase1/group-creation.png)

---

# File Services Baseline Configuration

## Shared Folder Creation

### Folder Information

```text
C:\SharedData
```

### Screenshot Placeholder

![Screenshot Placeholder](../screenshots/phase1/shared-folder-creation.png)

---

## SMB Share Configuration

### Share Information

```text
SharedData
```

### Screenshot Placeholder

![Screenshot Placeholder](../screenshots/phase1/smb-share-configuration.png)

---

## Permission Assignment

The FileShareUsers security group was assigned access permissions to the SharedData file share.

### Screenshot Placeholder

![Screenshot Placeholder](../screenshots/phase1/share-permissions.png)

---

# Script Execution

## PowerShell Execution Process

Configuration scripts were executed from elevated PowerShell sessions as required.

Execution order:

1. Windows Server (MIG-SRV01)
2. Windows Client (MIG-CLI01)

### PowerShell Commands

```powershell
# Insert commands used during execution
```

---

## Execution Log

### Reboots

> Document any required reboots.

### Warnings

> Document warnings encountered.

### Errors

> Document errors encountered.

### Successful Completion Indicators

> Document confirmation messages and validation output.

---

# Validation Testing

## Server Validation

### Successful Startup

* [ ] Server boots successfully

### Active Directory Validation

* [ ] Active Directory services operational

### DNS Validation

* [ ] DNS service operational

### Screenshot Placeholder

![Screenshot Placeholder](../screenshots/phase1/server-validation.png)

---

## Client Validation

### Successful Startup

* [ ] Client boots successfully

### Domain Join Verification

* [ ] Client joined to migration.local

### Authentication Verification

* [ ] Domain user login successful

### Screenshot Placeholder

![Screenshot Placeholder](../screenshots/phase1/client-validation.png)

---

## Network Validation

### Connectivity Testing

```powershell
ping MIG-SRV01
ping MIG-CLI01
```

### Name Resolution Testing

```powershell
nslookup migration.local
```

### Validation Checklist

* [ ] Ping successful
* [ ] Name resolution successful
* [ ] Network communication operational

### Screenshot 

![ Placeholder](../screenshots/phase1/network-validation.png)

---

## File Share Validation

### Validation Checklist

* [ ] Folder exists
* [ ] SMB share exists
* [ ] Permissions correctly applied
* [ ] Domain user can access share

### Screenshot 

![ Placeholder](../screenshots/phase1/file-share-validation.png)

---

# Issues Encountered

## Issue #1

### Issue Description

> Document issue here.

### Investigation

> Document investigation process.

### Actions Taken

> Document remediation steps.

### Resolution

> Document final outcome.

### Validation

> Document verification process.


---

# Conclusion

During Phase 1, I successfully established the baseline enterprise environment required for the Migration & Stabilization capstone. This phase included virtual machine deployment, operating system installation, network configuration, Active Directory implementation, user and group management, file services configuration, and system validation.

All required components were documented and verified to ensure the environment is stable, functional, and prepared for future migration activities. With the baseline environment established and validated, I am ready to proceed to Phase 2: Migration Event.
