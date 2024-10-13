# InfoGather Tool

InfoGather is a simple Bash script designed to gather various types of information about a domain or IP address. It allows users to perform DNS analysis, subdomain search, Nmap scans, and web server scans using Nikto.

## Features

- **DNS Analysis**: Retrieve the DNS A records for a given domain.
- **Subdomain Search**: Discover subdomains associated with a given domain.
- **Nmap Scan**: Perform a network scan to identify open ports and services.
- **Nikto Web Server Scan**: Scan a web server for vulnerabilities.

## Prerequisites

Before running the script, ensure you have the following tools installed on your system:

- `nslookup`
- `subfinder`
- `nmap`
- `nikto`

You can install them using your package manager. For example, on a Debian-based system, you can use:


sudo apt-get install dnsutils nmap nikto
For subfinder, you may need to install it via Go:

bash
Copier le code
go install github.com/projectdiscovery/subfinder/v2/cmd/subfinder@latest
Usage
Clone this repository to your local machine:

bash
Copier le code
git clone https://github.com/kingaka21/infogath.git
cd infogath
Make the script executable:


chmod +x infogath.sh
Run the script with the target domain or IP:


./infogath.sh <target_domain_or_ip>
Follow the prompts to choose the type of analysis you want to perform.


Copier le code
./infogath.sh example.com
You will be prompted to choose from the following options:

DNS Analysis
Subdomain Search
Nmap Scan
Web Server Scan with Nikto
Output
The results of each analysis will be saved in separate files located in the /root/mytool/infogath/<target_domain_or_ip>/ directory. The output files include:

dnsenum_result.txt
sublist3r_result.txt
nmap_result.txt
nikto_result.txt
