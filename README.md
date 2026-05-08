IT Helpdesk – 18 Day Windows Server & Active Directory Home Lab 

A fully hands-on IT lab that simulates a real-world enterprise helpdesk using VirtualBox and Windows Server 2022. 

📌 Project Overview

IT environment includes hands-on experience with Active Directory, Networking, Security Policies, Scripting (Windows PowerShell ISE), a fully functioning ticketing system (OSticket), and log analysis. This lab directory correlates with the daily responsibilities of IT Helpdesk or similarly related roles.  

Domain: alexlang-helpdesk.com 

OS: Windows Server 2022+ Windows 11 Pro 

Hypervisor: VirtualBox 

🛠️ Skills & Technologies  

🛠️ Skills & Technologies 

Column 1	Column 2
Category 	Tools / Concepts 
Virtualization 	VirtualBox, VM provisioning, VHD management, Guest Additions, network adapter modes 
Windows Server 	Windows Server 2022, Server Manager, SConfig, RDP 
Active Directory 	AD DS, domain promotion, OU structure, user & group management 
DNS 	Forward/Reverse Lookup Zones, A, CNAME, SOA, NS, SRV records 
DHCP 	Scope configuration, lease management, IP exclusions 
Group Policy 	GPO creation, password/lockout policy, software deployment, printer policy 
PowerShell 	Bulk user creation, password reset scripts, system info automation 
NTFS Permissions 	Inheritance, security groups, share permissions, effective access auditing 
Ticketing System 	osTicket, XAMPP/Apache, MySQL/phpMyAdmin 
Patch Management 	Action1 endpoint agent, vulnerability scanning, update deployment 
Backup & Recovery 	Shadow Copies, previous version restoration, Windows Server Backup 
Event Viewer 	Log filtering, custom views, Event IDs 4625/4740, .evtx export 


 

📅 Day-by-Day Summary 

Day 1 — VM Setup: Created a Windows Server 2022 using VirtualBox, resolved a display crash (switched to VMSVGA), and configured initial VM/Server settings via SConfig. 

Day 2 — Active Directory: Installed AD DS, promoted server to a Domain Controller, created forest alexlang-helpdesk.com,and used some command line Networking commands (whoami, net user, net accounts). 

Day 3 — Guest Additions: Installed VirtualBox Guest Additions and configured a host-to-VM shared folder. 

Day 4 — Users & Groups: Created a few domain users (John Stevens, Julie Foxburrow, Sully Johnson), a security group named IT_Help,and explored user property tabs and privilege settings. 

Day 5 — Workstation Deployment: Installed two Windows 11 Pro VMs simultaneously, used OOBE\BYPASSNRO to bypass Microsoft account requirements, and resolved a second VM boot failure via regedit. 

Day 6 — Domain Join & Networking: Configured static IPs, pointed DNS to the DC, joined both workstations to the domain, used ping and ipconfig /all to verify, and troubleshot a local vs. domain login issue. 

Day 7 — RDP & Group Policy: Enabled RDP, added the domain user to RDP users, connected remotely to test it, configured password/lockout policies via GPO (Group Policy Object), and verified with gpresult /R and net user commands. 

Day 8 — Patch Management: Deployed an Action1 agent to the DC (Domain Controller), identified 3 critical vulnerabilities and 7 missing updates on the first scan, and ran important updates to remediate these vulnerability alerts.  

Day 9 — Shared Folders: Created Tech and HelpDesk shares via the Server Manager, and configured share-level permissions restricting default access. 

Day 10 — Advanced GPO: Explored full GPME (Group Policy Management Editor) structure, configured screen saver timeout/display policies, and printer policies (browse URL, prevent deletion). 

Day 11 — DHCP: Installed the DHCP Server role, created a custom scope with IP range/lease/gateway, switched workstations to DHCP, and disabled the hypervisor's built-in DHCP to avoid IP conflicts. 

Day 12 — DNS: Reviewed AD auto-generated records (SOA, NS, SRV), created a custom A record, CNAME alias (files.alexlang-helpdesk.com), and a Reverse Lookup Zone. 

Day 13 — PowerShell Automation: Wrote scripts for bulk user creation (createUser.ps1), forced password reset (changeUser.ps1), and system info retrieval (SystemInfo.ps1), verified script results in AD. 

Day 14 — osTicket: Installed a XAMPP Server and osTicket, configured phpMyAdmin database and admin user, created departments (IT Support, Network Ops) and help topics, and troubleshot config file permissions and email validation errors. 

Day 15 — NTFS Permissions: Built departmental folder structure (HR, IT, Sales, Public). Created AD security groups per department, assigned NTFS permissions, and audited access using the Effective Access tab. 

Day 16 — Software Deployment: Deployed 7-Zip via GPO software installation policy using a domain-accessible MSI share and ran gpupdate /force — application auto-installed on reboot. 

Day 17 — Backup & Recovery: Set up Shadow Copies on the C: drive (daily at 2PM), deleted a test file and successfully restored it via the latest version of the C drive, and troubleshot a full backup failure due to insufficient VM disk space. 

Day 18 — Event Viewer & Log Analysis: Explored Windows Security logs. Triggered Event ID 4625 (failed logon) intentionally. Created a custom view for IDs 4625/4740. Exported logs as .evtx to simulate escalation workflow. 

🔑 Crucial Takeaways  

Real World Troubleshooting – Most of the days included some kind of issues (Software Bugs, Internet Issues, Security Migrations, etc) that each problem had to be troubleshot through and didn't have a linear solution and required multiple troubleshooting steps.  

Prioritizing Security (following Zero Trust Architecture ) - Maximizing security whenever possible, including: enforcing password complexity, lockout thresholds, NTFS permissions, following the principle of least privilege, and audit log monitoring  

Fully hands-on Environment Scope – Setup a fully networked domain with users, policies, shared resources, a full-fledged ticketing system, and monitoring 

PowerShell Scripting – PowerShell scripts were used for automating repetitive tasks such as user creation and password resets.  

Network Infrastructure Administration – Implemented and managed a full network, including configuring DHCP scopes and managing DNS records.  

Certifications in progress: 

Completed CompTIA A+ 

In progress CompTIA Network+ 
