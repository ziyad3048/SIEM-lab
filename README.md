# Security Monitoring and Vulnerability Management Report (SOC Report)

## Executive Summary
A security monitoring environment was established and configured using the Wazuh SIEM system to successfully integrate a Kali Linux host. The project focused on setting up an operational connection between the Wazuh Agent and Manager, followed by executing an end-to-end process for detecting and remediating security vulnerabilities on the target endpoint.

## Environment Setup
* Management System (Wazuh Manager): Server named node01
* Monitored Agent (Wazuh Agent): Kali Linux system with Agent ID: 001
* Connection Status: Active and successfully connected (Active / Connected)

## Executed Tasks & Workflow

### Phase 1: Agent Integration
* Operational Connection: Installed and activated the wazuh-agent on the Kali Linux system, ensuring stable telemetry and log shipping to the Wazuh Manager (node01).

### Phase 2: Vulnerability Detection & Management
1. Vulnerability Scanning:
   * Enabled the Vulnerability Detection module to scan the target system (Kali Linux).
   * Analyzed scan findings and identified a High Severity vulnerability (CVE-2025-60) associated with an outdated software package (weasyprint version 57.0).
   * Impact: The vulnerability allows an attacker to force weasyprint to send unauthorized network requests to local servers to obtain sensitive information.

2. Remediation & Hardening:
   * Executed security updates and package upgrades on the Kali Linux host to upgrade the package to version 60.0-2.
   * Rescanned the system to verify successful remediation and confirm host security posture hardening.
   * Result: Zero active vulnerabilities reported (0 Critical, 0 High, 0 Medium, 0 Low).

## Conclusion
The full SOC security response cycle was completed successfully by:
1. Ensuring stable connectivity and log flow between the agent and the SIEM manager.
2. Performing threat & vulnerability analysis, successfully patching CVE-2025-60, and mitigating potential security risks on the host.

## Technologies & Tools
* SIEM: Wazuh Manager & Agent
* OS: Kali Linux
* Module: Vulnerability Detector
* Skills: Vulnerability Assessment, Patch Management, Log Monitoring, Endpoint Hardening
