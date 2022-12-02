# MECM 5.0.2207.3

## [Download Here][Download]

[Download]: https://github.com/thekevinholman/MECM/archive/refs/heads/main.zip

### Microsoft Endpoint Configuration Manager (MECM) Management Pack  
### This MP Discovers and monitors MECM (Previously System Center Configuration Manager)

This MP is based on the previous System Center 2012 Configuration Manager MP

History:
* 5.0.2207.3 - Original release
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
