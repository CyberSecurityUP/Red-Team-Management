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

## Adversary Emulation Tools

|Name|Description|URL|
|-----|-----------|----|
|Stratus Red Team|Stratus Red Team is "Atomic Red Team™" for the cloud, allowing to emulate offensive attack techniques in a granular and self-contained manner.|https://github.com/DataDog/stratus-red-team|
|Prelude Operator|A Platform for Developer-first advanced security· Defend your organization by mimicking real adversarial attacks.|https://www.prelude.org/|
|Caldera|An automated adversary emulation system that performs post-compromise adversarial behavior within Windows Enterprise networks.|https://github.com/mitre/caldera|
|APTSimulator|A Windows Batch script that uses a set of tools and output files to make a system look as if it was compromised.|https://github.com/NextronSystems/APTSimulator|
|Atomic Red Team|Small and highly portable detection tests mapped to the Mitre ATT&CK Framework.|https://github.com/redcanaryco/atomic-red-team|
|Network Flight Simulator|flightsim is a lightweight utility used to generate malicious network traffic and help security teams to evaluate security controls and network visibility.|https://github.com/alphasoc/flightsim|
|Metta|A security preparedness tool to do adversarial simulation.|https://github.com/uber-common/metta|
|Red Team Automation (RTA)| RTA provides a framework of scripts designed to allow blue teams to test their detection capabilities against malicious tradecraft, modeled after MITRE ATT&CK.|https://github.com/endgameinc/RTA|

## Staging

|Name|Description|URL|
|-----|-----------|----|
|pwndrop|Self-deployable file hosting service for red teamers, allowing to easily upload and share payloads over HTTP and WebDAV.|https://github.com/kgretzky/pwndrop|
|C2concealer|A command line tool that generates randomized C2 malleable profiles for use in Cobalt Strike.|https://github.com/FortyNorthSecurity/C2concealer|
|FindFrontableDomains|Search for potential frontable domains|https://github.com/rvrsh3ll/FindFrontableDomains|
|Domain Hunter|Checks expired domains for categorization/reputation and Archive.org history to determine good candidates for phishing and C2 domain names|https://github.com/threatexpress/domainhunter|
|RedWarden|Flexible CobaltStrike Malleable Redirector|https://github.com/mgeeky/RedWarden|
|AzureC2Relay|AzureC2Relay is an Azure Function that validates and relays Cobalt Strike beacon traffic by verifying the incoming requests based on a Cobalt Strike Malleable C2 profile.|https://github.com/Flangvik/AzureC2Relay|
|C3|C3 (Custom Command and Control) is a tool that allows Red Teams to rapidly develop and utilise esoteric command and control channels (C2).|https://github.com/FSecureLABS/C3|
|Chameleon|A tool for evading Proxy categorisation|https://github.com/mdsecactivebreach/Chameleon|
|Cobalt Strike Malleable C2 Design and Reference Guide|Cobalt Strike Malleable C2 Design and Reference Guide|https://github.com/threatexpress/malleable-c2/|
|redirect.rules|Quick and dirty dynamic redirect.rules generator|https://github.com/0xZDH/redirect.rules|
|CobaltBus|Cobalt Strike External C2 Integration With Azure Servicebus, C2 traffic via Azure Servicebus|https://github.com/Flangvik/CobaltBus|
|SourcePoint|SourcePoint is a C2 profile generator for Cobalt Strike command and control servers designed to ensure evasion.|https://github.com/Tylous/SourcePoint|
|RedGuard|RedGuard is a C2 front flow control tool,Can avoid Blue Teams,AVs,EDRs check.|https://github.com/wikiZ/RedGuard|

## Command and Control

|Name|Description|URL|
|-----|-----------|----|
|Cobalt Strike|Cobalt Strike is software for Adversary Simulations and Red Team Operations.|https://cobaltstrike.com/|
|Empire|Empire 3 is a post-exploitation framework that includes a pure-PowerShell Windows agent, and compatibility with Python 3.x Linux/OS X agents.|https://github.com/BC-SECURITY/Empire|
|PoshC2|PoshC2 is a proxy aware C2 framework used to aid penetration testers with red teaming, post-exploitation and lateral movement.|https://github.com/nettitude/PoshC2|
|Koadic|Koadic C3 COM Command & Control - JScript RAT|https://github.com/zerosum0x0/koadic|
|merlin|Merlin is a cross-platform post-exploitation Command & Control server and agent written in Go.|https://github.com/Ne0nd0g/merlin|
|Mythic|A cross-platform, post-exploit, red teaming framework built with python3, docker, docker-compose, and a web browser UI.|https://github.com/its-a-feature/Mythic|
|Covenant|Covenant is a .NET command and control framework that aims to highlight the attack surface of .NET, make the use of offensive .NET tradecraft easier, and serve as a collaborative command and control platform for red teamers.|https://github.com/cobbr/Covenant|
|shad0w|A post exploitation framework designed to operate covertly on heavily monitored environments|https://github.com/bats3c/shad0w|
|Sliver|Sliver is a general purpose cross-platform implant framework that supports C2 over Mutual-TLS, HTTP(S), and DNS.|https://github.com/BishopFox/sliver|
|SILENTTRINITY|An asynchronous, collaborative post-exploitation agent powered by Python and .NET's DLR|https://github.com/byt3bl33d3r/SILENTTRINITY|
|Pupy|Pupy is an opensource, cross-platform (Windows, Linux, OSX, Android) remote administration and post-exploitation tool mainly written in python|https://github.com/n1nj4sec/pupy|
