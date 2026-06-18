# AI Enabled IT Support Capstone: Migration & Stabilization

## Table of Contents

* [Project Overview](#project-overview)
* [Business Application](#business-application)
* [Project Objectives](#project-objectives)
* [Environment](#the-virtual-environment)
* [Technologies Used](#technologies-used)
* [Project Phases](#project-phases)
* [Lessons Learned & Skills Demonstrated](#lessons-learned-and-skills-demonstrated)
* [My Troubleshooting Methodology](#my-troubleshooting-methodology)
---
# Project Overview

This repository documents my Per Scholas AI Enabled IT Support Capstone project. The project simulates a real-world enterprise migration event in which infrastructure changes introduce operational issues that require investigation, remediation, and validation. Throughout the project, I was responsible for building a virtual environment, executing migration activities, troubleshooting incidents, restoring services, validating outcomes, and documenting the entire process.

This repository serves as both a technical record of the project and a portfolio piece demonstrating my system administration, troubleshooting, and technical documentation skills.

---

# Business Application 

Organizations frequently undergo infrastructure changes that can introduce unexpected disruptions to users and business operations.

In this scenario, I assumed the role of an IT Support Specialist responsible for maintaining system stability before, during, and after a migration event. My responsibilities included preparing the environment, responding to incidents, restoring affected services, validating system functionality, and communicating results through professional documentation.

---

# Project Objectives

* Deploy and configure a Windows Server environment
* Deploy and configure a Windows Client workstation
* Establish domain services and network connectivity
* Perform migration-related activities
* Investigate and resolve system issues
* Validate functionality after remediation
* Produce professional technical documentation
* Demonstrate enterprise troubleshooting methodologies

---

# The Virtual Environment

## Infrastructure

| Component       | Description                              |
| --------------- | ---------------------------------------- |
| Hypervisor      | VirtualBox                               |
| Server OS       | Windows Server 2022                      |
| Client OS       | Windows 11                               |
| Network Type    | Internal Virtual Network                 |
| Domain Services | Active Directory Domain Services  |

## Network Configuration


### Network Diagram

```text
+------------------+
|        TBD       |
+------------------+
```

---

# Technologies Used

| Technology       | Purpose                        |
| ---------------- | ------------------------------ |
| Windows Server   | Server operating system        |
| Windows Client   | Workstation operating system   |
| Active Directory | Identity and access management |
| DNS              | Name resolution                |
| DHCP             | IP address management          |
| Group Policy     | Centralized configuration      |
| PowerShell       | Administration and automation  |
| VirtualBox       | Virtualization platform        |

---

# Project Phases

## [Phase 1](Documentation/Phase1.md) – Environment & Baseline Setup
Establish and document a stable enterprise environment.

### Deliverables

* Server deployment
* Client deployment
* Network configuration
* Baseline validation

---

## [Phase 2](Documentation/Phase2.md) - Migration Event

Execute migration-related changes and document system impact.

### Deliverables

* Migration execution
* Configuration updates
* Initial validation testing

---

## Phase 3 – Incident Response
<!--
[Phase 3](Documentation/Phase3.md) - Incident Response
-->

Investigate and diagnose user-reported issues. 

### Deliverables

* Ticket analysis
* Root cause identification
* Troubleshooting documentation

---

## Phase 4 – Stabilization & Recovery
<!--
[Phase 4](Documentation/Phase4.md) - Stabilization & Recovery
-->

Implement corrective actions and restore system stability.

### Deliverables

* Remediation activities
* Service restoration
* Validation testing

---

## Phase 5 – Reporting & Presentation
<!--
[Phase 5](Documentation/Phase5.md) – Reporting & Presentation
-->

Communicate findings, lessons learned, and project outcomes.

### Deliverables

* Technical report
* Executive summary
* Final presentation

---
# Lessons Learned and Skills Demonstrated
| Technical Domain                    | Skills Demonstrated                                                                            |
| ----------------------------------- | ---------------------------------------------------------------------------------------------- |
| Windows Server Administration       | Server deployment, hostname configuration, static IP addressing, server role installation      |
| Windows Client Administration       | Client deployment, workstation configuration, domain integration                               |
| Active Directory                    | Domain Controller deployment, domain administration, user and group management                 |
| DNS Services                        | DNS configuration, name resolution, domain service support                                     |
| Identity & Access Management        | User provisioning, group membership management, permission assignment                          |
| File Services                       | SMB share configuration, access control, resource management                                   |
| Troubleshooting & Incident Response | Incident investigation, evidence collection, root cause analysis, corrective action planning   |
| System Validation                   | Connectivity testing, authentication testing, service verification, resource access validation |
| PowerShell Administration           | System configuration, diagnostics, validation, administrative automation                       |
| Virtualization                      | Oracle VirtualBox deployment, virtual machine configuration, environment management            |
| Technical Documentation             | Change tracking, incident documentation, migration reporting, validation reporting             |
---

# My Troubleshooting Methodology

The following process was used throughout the project:

## 1. Issue Identification

Document symptoms and collect initial information.

## 2. Investigation

Review logs, configurations, and system behavior.

## 3. Remediation

Implement corrective actions based on findings.

## 4. Validation

Confirm resolution using testing and verification procedures.

---
