**Title:** DDoS (Distributed Denial of Service) Attack Runbook

**Version:** v2.6.10-IR

**Owner:** Alonzo Villanueva

**Last Reviewed:** 2025-12-03

**1. Introduction**

- **Mission:** Declare the DDoS incident and activate the runbook. Coordinate communication between SOC, Network Engineers, and Incident Management Team.
- **Audience:** Network Engineers, Security Analysts, and System Administrators, Incident management team
- **TL; DR:** Acquire, Preserve, Document Evidence> Contain the Incident> Eradicate the Incident> Recover from Incident> Post Incident Documentation (postmortem and feedback process)

**2. Scope & Activation Criteria**

- **Applies To:** Incident Commander, SOC Tier 2, Network Engineering, Cloud/ISP partner
- **Do NOT Use When:** When the event is part of another type of incident. When the traffic pattern does not match DDoS characteristics
- **Activate When:**
- Unusual traffic patterns (sudden spikes in connection attempts, packet rate, or bandwidth usage)
- Automated alerts from DDoS protection services indicate active mitigation
- Monitoring tools that have predefined thresholds begin to exceed

**3. High-Level Steps**

- Acquire, Preserve, Document Evidence
- Contain the incident
- Eradicate the incident

**4. Detailed Procedure**

**4.1 Establish Communication Protocols**

a. Establish clear communication protocols to ensure that all stakeholders are informed and coordinated during this event. Includes internal communication among team members and external communication with clients and customers. Which should specify channels and methods of communication to be used during the event, ensuring information flow and preventing panic or even misinformation.

b. Developing communication protocols involves identifying key stakeholders and assigning communication responsibilities to the entire team regarding the safety of Information security.

c. **Validation:** Reading the response plan that was explained in policy and training for each position in the company/corporation. Each group of positions shall have quick channels towards a contact list in the event of the DDoS. Which gives proper communication. This transparency helps maintain trust with external partners to minimize damage towards organizations' reputation.

**4.2 Containment & Mitigation**

a. Implement Traffic Filtering: involves selectively allowing or blocking specific types of network traffic based on predefined criteria. Deployment of real time analytics and automated rules to promptly adapt filtering criteria as an attack unfolds. This implementation of granular filtering rules can improve precision of blocking malicious packets while maintaining essential service operations

b. Active Rate Limiting: Rate limiting controls the number of requests a user can make to a network service within a specified timeframe. Restricting request rates protects us from being overwhelmed by excessive traffic, allowing legitimate users access the service unhindered. Balance security measures with user experience, ensuring limits are stringent enough to reduce impact with deterring genuine use.

c. Engaging DDoS Protection Services: Activate services that specialize in absorbing and filtering malicious traffic before reaching the targeted system, providing another line of defense. Leverage global networks and advanced analytics to identify and neutralize threats. Integrate with existing security infrastructure which should be seamless, with clean and trained protocols for rapid activation.

**4.3 Eradication and Recovery**

a. Remove Malicious Artifacts: Conduct thorough system scans for malware or rogue files. Which prevents persistent vulnerabilities or even footholds for future attacks. Effective removal entitles comprehensive scanning with updated malware tools that can detect and eliminate known and emerging threats. Collaboration with IT departments to ensure swift aid for identification and resolution for vulnerabilities.

b. Restore Services: Once threats are neutralized and systems are verified of malicious artifacts. Restoration efforts prioritize critical services first, ensuring most important functionalities are operational ASAP. Involve stakeholders and outline communication protocols to update users on progress.

c. Monitor Post Recovery: Once services are restored, close observation of system performance and traffic patterns is necessary to identify and lingering issues or vulnerabilities. These steps help detect anomalies and confirm that defense against similar future attacks is intact. Effective post recovery monitoring involves establishing thresholds to quickly detect unexpected changes. Regularly reviewing logs and alerts can provide insights into system behavior, while periodic stress testing can validate ongoing resilience.

d. Conduct Post-Mortem Review: Involving stakeholders who discuss the effectiveness of the response plan and pinpoint any shortcomings. Documenting detailed insights helps refine future incident responses and contribute to strategic deterrence measures. Conducting a comprehensive post-mortem analysis requires clear guidelines to evaluate all aspects of the incident, from initial detection to final recovery.

**5. Completion Checklist**

- Services remained available. Critical services remained available with minor spikes and latency when trying to login or refresh to dashboard.
  - Malicious Traffic Identified- attack type confirmed DDoS. Filtering and rate limiting successfully reduces malicious traffic without harming legitimate users. No Collateral damage to internal systems or clients.
- Clear communication and Coordination Occurred.
  - Stakeholders were informed appropriately (SOC, NOC, ISP/Cloud provider)
  - No communication gaps or delays.
- Evidence Logging: timeline documentation requirements included. Storage location for packet captures and dashboards documented.
- Detection Thresholds Need adjustment
  - Baselines are too loose
  - Additional telemetry will be needed
- Mitigation steps must be faster
  - Rate limiting may need predefined templates

**6. References**

- <https://github.com/aws-samples/aws-incident-response-playbooks/blob/master/playbooks/IRP-DoS.md> - This template matters because it's a template provided to customers using AWS products and who build their incident response capabilities.
- <https://www.onpage.com/a-process-for-ddos-incident-response/> - Article that will improve the planning, execution and steps on handling this event in a timely, professional and effective way.

**7\. Change History**

V2.6.10 2025-12-03 Incident Response Management Added New attack indicators
