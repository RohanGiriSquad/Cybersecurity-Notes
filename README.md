# Cybersecurity-Notes


# Web Application Security Notes

## Top 10 Ports and Services

1. **FTP**:
   - Port: 20 & 21
   - Service: File Transfer Protocol

2. **SSH**:
   - Port: 22
   - Service: Secure Shell / Secure Socket Shell / Remote Login (rlogin) / Remote Shell (rsh) / Remote Copy (rcp) / Remote Distribution (rdist)

3. **TELNET**:
   - Port: 23
   - Service: Telecommunication Network / Terminal Network

4. **SMTP**:
   - Port: 25
   - Service: Simple Mail Transfer Protocol

5. **DNS**:
   - Port: 53
   - Service: Domain Name System

6. **DHCP**:
   - Ports: 67 & 68
   - Service: Dynamic Host Configuration Protocol

7. **HTTP**:
   - Port: 80
   - Service: Hypertext Transfer Protocol

8. **HTTPS**:
   - Port: 443
   - Service: Hypertext Transfer Protocol Secure

9. **POP3**:
   - Port: 110
   - Service: Post Office Protocol

10. **NNTP**:
    - Port: 119
    - Service: Network News Transfer Protocol

11. **IMAP**:
    - Port: 143
    - Service: Internet Message Access Protocol

## OSI Model

- **Physical Layer**: Deals with transmission modes (simplex, half-duplex, full-duplex).
- **Data Link Layer**: Contains MAC (Media Access Control) and LLC (Logical Link Control).
- **Network Layer**: Involves logical addressing and switching.
- **Transport Layer**: Ensures reliable data transfer.
- **Session Layer**: Manages sessions between applications.
- **Presentation Layer**: Handles data representation and encryption.
- **Application Layer**: Provides interfaces for network applications.

## Proxy Types

1. Anonymous Proxy
2. SSL Proxy
3. Transparent Proxy
4. Reverse Proxy
5. Forward Proxy

## VPN Types

1. Site-to-Site VPN
2. IPsec VPN
3. SSH VPN
4. L2TP
5. PPTP
6. OpenVPN
7. SSL and TLS VPN

## Password Attacks Tools

- John the Ripper
- hashcat
- Hydra
- ophcrack
- Ncrack
- WGen
- SSH Auditor

## Blind SSRF

Blind SSRF (Server-Side Request Forgery) occurs when an attacker can make a server perform HTTP requests to arbitrary destinations without receiving direct responses.

## Web Cache Deception

Web Cache Deception involves tricking a caching proxy into improperly storing sensitive data, which an attacker can then retrieve from the cache.

## Exploiting Signup/Register Functionality

1. Injection Attacks (SQLi, XSS)
2. Duplicate Registration
3. No Rate Limit
4. Weak Password Policies
5. Insecure Direct Object References (IDOR)
6. CAPTCHA Bypass
7. Insufficient Email Verification


## Reconnaissance Tools

### Port Scanning Tools
- Nmap
- Masscan
- Naabu

### Subdomain Enumeration
- Altdns
- Amass
- Aquatone
- DNSRecon

### Vulnerability Scanner
- Nessus
- Nuclei
- DalFox XSS Scanner
- SQLMap

### Search Engine Tools
- Shodan
- Censys
- Google Dorks
- FOCA

### Directory Enumeration
- FFuF
- Dirb
- Gobuster
- Dirsearch
- Dirbuster

## Bug Bounty Tips

- Utilize Google Dorking to find hidden resources and vulnerabilities.
- Exploit signup vulnerabilities like SQL injection, XSS, or weak passwords.
- Look for Blind SSRF vulnerabilities to cause servers to make unauthorized requests.
- Exploit Web Cache Deception by tricking caching proxies into storing sensitive data.
- Utilize recon tools for discovering hosts, subdomains, and vulnerabilities in target applications.

## Getting Started with Bug Bounty

1. Learn networking basics and common web technologies.
2. Study security concepts and common vulnerabilities.
3. Explore bug bounty resources such as books, YouTube channels, and practice platforms.
4. Start practicing with labs and platforms like PortSwigger Academy, Pentester Lab, TryHackMe, and Hack The Box.

## Password Attacks

Use tools like John the Ripper, hashcat, and Hydra to crack passwords and create wordlists. These tools can help test the strength of passwords and identify weak authentication mechanisms.

## XSS to Account Takeover (ATO)

Exploit XSS vulnerabilities to escalate to an Account Takeover (ATO) by stealing session IDs, initiating ATO via email invites, manipulating security questions, or adding authentication methods.

## Web Cache Deception Exploitation

Exploit Web Cache Deception vulnerabilities by tricking caching proxies into storing sensitive data and gain unauthorized access to cached information.

## Google Dorking for Hidden Resources

Use Google Dorking to discover hidden log files, webcams, passwords, and other sensitive information exposed on the internet.

## Exploiting Signup/Register Functionality

Test signup/register functionality for injection attacks, duplicate registration, rate limiting bypass, weak password policies, insecure direct object references (IDOR), CAPTCHA bypass, and insufficient email verification.

## Blind SSRF

### Definition
Blind SSRF (Server-Side Request Forgery) is an attack where an attacker can cause a vulnerable server to make HTTP requests to arbitrary destinations without directly receiving the responses.

### Techniques for Finding Blind SSRF
- Out-of-Band Techniques: Utilize external services or resources to confirm SSRF vulnerability and exfiltrate data without directly receiving responses.

## XXE (XML External Entity) Vulnerabilities

### Areas to Look for XXE Vulnerabilities
1. Web Applications: Including SOAP and RESTful web services, XML-based APIs, and applications parsing XML input.
2. File Upload Forms: Upload crafted XML files containing external entity references and observe server responses.
3. Document Processing Libraries: Libraries and software parsing XML documents may contain XXE vulnerabilities.
4. XML-RPC and SOAP Endpoints: Send XML requests with crafted external entity references and analyze server responses.
5. Third-Party Plugins and Libraries: Review third-party code for XML parsing functionalities.
6. Content Management Systems (CMS): CMS platforms processing XML data may be susceptible to XXE vulnerabilities.
7. Mobile Applications: Applications accepting XML input, communicating with XML-based APIs, or parsing XML data might be vulnerable.

## Exploiting SQL Injection (SQLi)

### Steps to Get Your First SQLi
1. Use Waybackurls to gather all possible URLs of the target.
2. Use GF tool to filter SQL parameters of the target and save them.
3. Exploit SQL injection vulnerabilities in input fields to manipulate the database or gain unauthorized access.

## Web Cache Deception

### Overview
Web Cache Deception (WCD) is an attack where an attacker tricks a caching proxy into improperly storing private information, gaining unauthorized access to cached data.

### Exploitation Techniques
1. Exploit the caching of static and public files like stylesheets, scripts, and images.
2. Inject malicious content into web applications to manipulate caching behavior.
3. Use out-of-band techniques to exfiltrate cached data without directly receiving responses.

## Signup/Register Functionality Exploitation

### Vulnerabilities to Test For
1. Injection Attacks: SQL injection, XSS.
2. Duplicate Registration: Allow multiple sign-ups using identical credentials.
3. No Rate Limit: Lack of rate limiting on signup page can lead to fake account generation.
4. Weak Password Policies: Lack of complexity requirements and multi-factor authentication.
5. Insecure Direct Object References (IDOR): Manipulate parameters to gain unauthorized access.
6. CAPTCHA Bypass: Exploit flaws in CAPTCHA implementation.
7. Insufficient Email Verification: Lack of or weak email verification mechanisms.

## Password Attacks

### Tools for Password Cracking
- John the Ripper: A fast password cracker written in C.
- Hashcat: World's fastest and most advanced password recovery utility.
- Hydra: Parallelized login cracker supporting numerous protocols.
- Ophcrack: Windows password cracker based on rainbow tables.
- Ncrack: High-speed network authentication cracking tool.
- WGen: Python tool for creating wordlists.
- SSH Auditor: Scans for weak SSH passwords on networks.

## Blind SSRF Exploitation Techniques

### Out-of-Band Techniques
Out-of-Band SSRF exploitation involves using external services or resources to confirm SSRF vulnerability and exfiltrate data without directly receiving responses from the server.

## Bug Bounty Tips

### SQL Injection (SQLi)
- Check state-changing requests like POST, DELETE, PUT for SQL injection vulnerabilities.
- Test parameters with string input for context breaking with ' or #.

### Bug Bounty Resources
- Study networking basics, web technologies, and security concepts.
- Refer to books, YouTube channels, expert write-ups, articles, and blogs.
- Practice on platforms like PortSwigger Academy, Pentester Lab, and Hack the Box.

## XXE (XML External Entity) Vulnerabilities

### Areas to Look for XXE Vulnerabilities
- Web Applications
- File Upload Forms
- Document Processing Libraries
- XML-RPC and SOAP Endpoints
- Third-Party Plugins and Libraries
- Content Management Systems (CMS)
- Mobile Applications

## Exploiting SQL Injection (SQLi)

### Steps to Get Your First SQLi
1. Use Waybackurls to gather all possible URLs of the target.
2. Use GF tool to filter SQL parameters of the target and save them.

## Web Cache Deception

### Exploitation Techniques
1. Exploit caching of static and public files.
2. Inject malicious content into web applications.
3. Use out-of-band techniques to exfiltrate cached data.

## Signup/Register Functionality Exploitation

### Vulnerabilities to Test For
1. Injection Attacks
2. Duplicate Registration
3. No Rate Limit
4. Weak Password Policies
5. Insecure Direct Object References (IDOR)
6. CAPTCHA Bypass
7. Insufficient Email Verification
