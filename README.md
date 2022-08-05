# ActiveDirectoryAttackTool


ActiveDirectoryAttackTool (ADAT) tool is used to assist CTF players and Penetration testers with helpful commands to run against an Active Directory Domain Controller. This tool is best utilized using a set of known working credentials against the host.
<br/>

# Usage: General

Standard usage
```
bash ADAT.sh -u ViperOne -p Password123 -t 10.10.10.100 -d Security.local
```
<br/>

Usage with LDAP base search
```
bash ADAT.sh -u ViperOne -p Password123 -t 10.10.10.100 -d Security.local -l "DC=Security,DC=Local"
```
<br/>

Usage with GitHub for script repositories (Target system has internet access)
```
bash ADAT.sh -u ViperOne -p Password123 -t 10.10.10.100 -d Security.local
```
<br/>

# Usage: Systems with no internet access
If the system you are testing has no internet access or is a CTF machine, ADAT will download the required GitHub repositories to your attacking system. Ensure you specify the ```-L``` parameter and set both the LocalIP and LocalPort variables within the script to that of your attacking system.
```
bash ADAT.sh -u ViperOne -p Password123 -t 10.10.10.100 -d Security.local -L
```
ADAT will run a http python3 server on the attacking system using the LocalIP and LocalPort parameters.

<br/>

# Usage: Standalone Windows Systems

Usage for non domain joined systems, whilst not officially supported by ADAT, many of the commands can be run against a standalone Windows system.
```
bash ADAT.sh -u ViperOne -p Password123 -t 10.10.10.100 -d . -L
bash ADAT.sh -u ViperOne -p Password123 -t 10.10.10.100 -d WORKGROUP -L
```
<br/>

# Supported Protocols
Some of the protocols ADAT prints out commands for:

- DNS
- Kerberos
- LDAP
- MSSQL
- NTP
- RDP
- SMB
- WinRM
<br/>

# Supported Tools
Some of the tools ADAT prints out commands for:

- BloodHound
- Crackmapexec (Including modules and PowerShell commands)
- Impacket toolset
- Metasploit
- Nmap
- ldapdomaindump
- ldapsearch
- pywerview
- xfreerdp
<br/>


ADAT produces commands for both external and internal usage.
<br/>

# OSCP

ADAT is OSCP friendly, the commands it prints out might not be. Please be cautious about what commands and scripts invoke before running in an exam environment.