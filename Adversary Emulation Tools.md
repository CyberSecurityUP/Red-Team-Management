## What is Adversary Emulation?

Adversary emulation leverages adversary tactics, techniques, and procedures, enhanced by cyber threat intelligence, to create a security test based on real world intrusion campaigns.

Security tests using adversary emulation identify gaps, verify defensive assumptions, and prioritize resources. Red teams and penetration tests often cover identification and verification, but when it comes to prioritizing organizational needs and budgets they typically fall short. Traditionally, these approaches have also not focused on answering questions like

“Could that attack that we saw in the news have happened to us?”

or 

“What would happen if our systems were targeted by an organized crime group looking to profit from ransomware?”

Adversary emulation helps organizations focus their security testing to prioritize threats that their defenders may face each day.

Successful adversary emulation is a collaborative effort between multiple cybersecurity domains of expertise, particularly red team and cyber threat intelligence (CTI) professionals. CTI professionals work with the security operations center (SOC) and senior leadership to determine what types of threats might target the organization, while red teams work to test and probe defenses. Red teams have the tradecraft and skillset to perform malicious actions to subvert defenses, but that expertise is far more valuable to organizations trying to understand the implications of red team findings on their security posture when it is tied to real world threat data. 

Previously, the synthesis of CTI and red teaming was more challenging due to a lack of readily available data and a consistent way to share information. In 2016, the MITRE Corporation released the very first version of ATT&CK, a framework which served as a foundation for information sharing related to adversary behaviors. ATT&CK’s success is driven by the community contributions of organizations world-wide, enabling adversary data coverage unlike anything previously seen. The tactics and techniques in ATT&CK have been identified in real world intrusions, making them ideal candidates for emulations. New adversary campaigns can be mapped to ATT&CK and shared so that others can emulate adversaries of interest to their organization.

by Scythe

## Adversary Emulation Plan

To showcase the practical use of ATT&CK for offensive operators and defenders, MITRE created Adversary Emulation Plans. These are prototype documents of what can be done with publicly available threat reports and ATT&CK. The purpose of this activity is to allow defenders to more effectively test their networks and defenses by enabling red teams to more actively model adversary behavior, as described by ATT&CK. This is part of a larger process to help more effectively test products and environments, as well as create analytics for ATT&CK behaviors rather than detecting a specific indicator of compromise (IOC) or specific tool.

There are many threat intel reports that focus on malware reverse engineering, initial compromise, and command and control (C2) explanations; however, there are not many threat reports on how attackers are chaining techniques together or how attackers operate on keyboard. Because these prototypes are built on these open threat reports, they have the same limitations. To help with this, we provided a sample way to string the ATT&CK tactics together based on general red teaming experience. To create these plans, the team drilled down on specific APT groups listed in ATT&CK and see what kind of plans could be generated for an operator to emulate those APTs. After reading what capabilities were provided by an APT's tools, we compiled a list of other ways to exhibit the same behavior. We wanted operators to behave generally like a specific adversary (sticking to that adversary's known TTPs and behaviors), but having some latitude in actual implementation. To help with this, we also provided a cheat sheet for commands that can be executed for similar behavior in some of the most commonly used red teaming tools. A sample, high level diagram is highlight below as one possible way to structure an APT3 emulation plan.

by Mitre Att&ck

