BluBlood
========
This repository is an edit of the BadBlood scripts by Secframe. The goal is to build an Active Directory Domain that is vulnerable for testing password spraying, AS-REP Roasting, etc. After running ran on a domain, security analysts and engineers can practice using tools to gain an understanding and prescribe to securing Active Directory. Each time this tool runs, it produces different results.



## Automation

### Vagrant
A local copy of this repo on a host can be copied to a Vagrant guest by adding the following line in the ```Vagrantfile```:
``` config.vm.provision "file", source: "~/git/BadBlood", destination: "$HOME/BadBlood" ``` and issuing ```vagrant provision``` 
($HOME/BadBlood = c:\users\vagrant\BadBlood)

### [Splunk Attack Range](https://github.com/splunk/attack_range) 
Provides examples of executing this repo using Ansbile for automated AD setup

## Installation

Requirements:
- Domain Admin and Schema Admin permissions
- Active Directory Powershell Installed

Running On Windows:
```
# clone the repo
# Run Invoke-badblood.ps1
./badblood/invoke-badblood.ps1
# Optional: Run with parameters; Use "-NonInteractive" for scripting
./badblood/invoke-badblood.ps1 -UserCount 50
```
## Acknowledgments (from the original author)
I'd like to send thanks to the countless people who wanted this as a product and waited while I made it!

## License
This project is licensed under the gplv3 License - see the LICENSE.md file for details

## Disclaimer
Please note: all tools/ scripts in this repo are released for use "AS IS" without any warranties of any kind, including, but not limited to their installation, use, or performance. We disclaim any and all warranties, either express or implied, including but not limited to any warranty of noninfringement, merchantability, and/ or fitness for a particular purpose. We do not warrant that the technology will meet your requirements, that the operation thereof will be uninterrupted or error-free, or that any errors will be corrected.

Any use of these scripts and tools is at your own risk. There is no guarantee that they have been through thorough testing in a comparable environment and we are not responsible for any damage or data loss or time loss incurred with their use.

You are responsible for reviewing and testing any scripts you run thoroughly before use in any non-testing environment.  This tool is not designed for a production environment.


