# Custom Sigma Detection Rules Repository

A centralized, version-controlled repository for custom, high-signal [Sigma rules](https://github.com/SigmaHQ/sigma). 
These rules are designed to bridge the gap between offensive emulation validation (via frameworks like Atomic Red Team) and defensive telemetry verification.


Used (https://sigconverter.io) to test rules(target splunk).

Alternative method:
Prerequisites

Install the Sigma compiler utility via Python:
Bash

pip install sigma-cli

Compilation Examples

Convert a rule inside this repository to target query syntax: (using t1082.yaml as example).

To Microsoft Sentinel (KQL):
Bash

`sigma convert -t microsoft365_defender -p sysmon rules/windows/sysmon/t1082.yaml`

To Splunk SPL:
Bash

`sigma convert -t splunk -p sysmon rules/windows/sysmon/t1082.yaml`

To Elastic Query Language (EQL):
Bash

`sigma convert -t elasticsearch -p sysmon rules/windows/sysmon/t1082.yaml`
