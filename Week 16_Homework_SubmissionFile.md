## Week 16 Homework Submission File: Penetration Testing 1

#### Step 1: Google Dorking


- Using Google, can you identify who the Chief Executive Officer of Altoro Mutual is:
 
Karl Fitzgerald

- How can this information be helpful to an attacker:

For the planning and reconnaissance stage will be helpful, and as well for social engineering and try to guest credentials like login in the server.

#### Step 2: DNS and Domain Discovery

Enter the IP address (65.61.137.117) for `demo.testfire.net` into Domain Dossier and answer the following questions based on the results:

  1. Where is the company located: 

City: Sunnyvale
State/Province: CA
Postal Code: 94085
Country: US

  2. What is the NetRange IP address:

NetRange:       65.61.137.64 - 65.61.137.127

  3. What is the company they use to store their infrastructure:

 Rackspace Backbone Engineering


  4. What is the IP address of the DNS server:

65.61.137.117

#### Step 3: Shodan

- What open ports and running services did Shodan find:

Open Ports: 80; 443; 8080.

Apache Tomcat/Coyote JSP engine1.1

#### Step 4: Recon-ng

- Install the Recon module `xssed`. 
- Set the source to `demo.testfire.net`. 
- Run the module. 

Is Altoro Mutual vulnerable to XSS: YES



### Step 5: Zenmap

Your client has asked that you help identify any vulnerabilities with their file-sharing server. Using the Metasploitable machine to act as your client's server, complete the following:

- Command for Zenmap to run a service scan against the Metasploitable machine: 
 
nmap -T4 -A -v 192.168.0.10

- Bonus command to output results into a new text file named `zenmapscan.txt`:

nmap -T4 -A -v -oN zenmapscan.txt 192.168.0.10

- Zenmap vulnerability script command:

nmap --script samba-vuln-cve-2012-1182 192.168.0.10
 

- Once you have identified this vulnerability, answer the following questions for your client:

  1. What is the vulnerability:

Samba 3.0.x - 3.6.3 (inclusive)

  2. Why is it dangerous:

Samba versions 3.6.3 and all versions previous to this are affected by
a vulnerability that allows remote code execution as the "root" user
from an anonymous connection.

  3. What mitigation strategies can you recommendations for the client to protect their server:

Patches addressing this issue have been posted to:

    http://www.samba.org/samba/security/

Additionally, Samba 3.6.4, Samba 3.5.14 and 3.4.16 have been issued as
security releases to correct the defect. Patches against older Samba
versions are available at:

    http://samba.org/samba/patches/

Samba administrators running affected versions are advised to upgrade
to 3.6.4, 3.5.14, or 3.4.16 or apply these patches as soon as
possible.

---
© 2020 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.  

