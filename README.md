# MCM 5.0.2303.0

## [Download Here][Download]

[Download]: https://github.com/thekevinholman/MECM/archive/refs/heads/main.zip

### Microsoft Configuration Manager (MCM) Management Pack  
### This MP Discovers and monitors MCM (Previously Microsoft Endpoint Configuration Manager / System Center Configuration Manager)

This MP is based on the previous System Center 2012 Configuration Manager MP

History:
* 5.0.2303.0 - 5/3/23
  * Rebranded MP to Microsoft Configuration Manager
  * Changed the default service monitor for PXE role to monitor (SccmPxe) service and disabled the (wdsserver) service monitor by default.  If you still use WDSSERVER service, please enable that monitor and disable (SCCMPXE) service monitor targeting the PXE server role.
  * Fixed displayname for PXE rollup monitor
  * Fixed mispellings for "Secondary"
  * Updated references to support import in SCOM 2012R2
* 5.0.2211.0 - 1/25/23
  * Reduced frequency of MECM Client Discovery from 60 seconds to once a day.
  * Created an override to disable the SMSExec service monitor for members of the Site Database Computers Group, since this was causing false alarms as Database servers are not typically Site server roles with SMSExec service present.
* 5.0.2207.3 - Original release - 12/2/22
  * MECM Client Class discovers sitecode and version properties
  * Fixed errors on MECM client discovery
  * Added MatchCount property to most monitors to support multiple consecutive samples to reduce noise
  * Removed overrides that were muting alerts from unit monitors
  * Added overrides to disabled alerts from the aggregate rollup monitors and dependency rollup monitors
  * Added ScaleBy to Process based CPU Rules and Monitors so they actually work.
  * Changed Max sample separation on Perf Collection rules from 10 to 4 so one data point will be collected every hour on any perf collection rules that are enabled.
  * Deleted all Manual Reset Monitors and replaced with Rules.
  * Deleted all Classes, Rules, and Monitors for Deprecated and Unsupported roles  
  * Renamed all Element ID's to include the MP ID, and follow structured rules:
    * Datasource ends with .DS and with Displaystring Datasource
    * ProbeAction ends with .PA and with Displaystring Probe Action
    * WriteAction ends with .WA and with Displaystring Write Action
    * MonitorType ends with .MT and with Displaystring MonitorType
    * Discovery ends with .Discovery and with Displaystring Discovery
    * Rule ends with .Rule and with Displaystring Rule
    * Monitor Ends with .Monitor and with Displaystring Monitor
    * Aggregate Monitor ends with .AggregateRollup.Monitor
    * Dependency Monitor ends with .DependencyRollup.Monitor
    * Groups end with .Group and with Displaystring Group
    * Task ends with .Task
  * Removed all Override Displaystrings which were pointless
