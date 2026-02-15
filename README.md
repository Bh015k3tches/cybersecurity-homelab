# cybersecurity-homelab
Hands-on cybersecurity home lab documenting virtual machines, Linux practice, networking, and security projects using Kali Linux and VirtualBox.
## Lab 1 – Kali Linux Virtual Machine Setup

Goal:
Create a virtual machine to use as a security testing environment.

Tools Used:

* VirtualBox
* Kali Linux (ARM64)

Steps Taken:

* Installed VirtualBox on macOS
* Downloaded Kali Linux ARM64 image
* Imported the Kali VM into VirtualBox
* Allocated RAM and CPU cores
* Booted and verified the system worked

Result:
Successfully ran Kali Linux inside a virtual machine.

What I Learned:

* How virtual machines work
* Difference between host OS and guest OS
* Basic VM configuration (CPU, RAM, booting)
* Why ARM64 matters on Apple Silicon

**Next Steps:**

* Practice Linux commands
* Configure networking
* Begin network scanning with Nmap

  

<img width="812" height="850" alt="Screenshot 2026-02-14 at 6 41 34 PM" src="https://github.com/user-attachments/assets/8eb39629-8f17-45a0-8eba-7b56b8a7cc66" />
<img width="922" height="779" alt="Screenshot 2026-02-14 at 6 42 02 PM" src="https://github.com/user-attachments/assets/f54d89c0-16a9-4875-b6ac-2b0d924b68e4" />






Lab 2 – Basic Network Scanning with Nmap

Goal: Identify active hosts and open ports within a private subnet.

Tools Used:

Kali Linux

Nmap

Steps Taken:

1.Checked the VM’s network configuration using ip a to find the subnet.
2.Installed Nmap (sudo apt install nmap -y).
3.Performed a basic service scan:
   -sudo nmap -sV 10.x.x.x.x
4.Observed the output, noting active hosts and open ports.

Result:
Discovered 3 active hosts.
Open ports found: 5000, 7000, 8021.

What I Learned:
How to scan a subnet for live hosts.
How to identify open ports and basic service info.
The difference between open, closed, and filtered ports.
How to interpret scan output for practical analysis.

Next Steps:

Perform a more detailed scan with OS detection and service scripts.
Document findings professionally for GitHub.




Lab 3 – DNS Service Verification

Goal: Verify that network services are operational and understand their purpose.

Tools Used:
Kali Linux
nslookup
dig

Steps Taken:
Identified DNS service on port 53 from previous Nmap scan.
Tested DNS functionality using:
nslookup google.com
dig google.com
Recorded the resolved IP addresses and analyzed the responses.

Result:
Verified that DNS service responded correctly to queries.
Successfully resolved domain names to IP addresses.

What I Learned:
How DNS works and why port 53 is important.
How to use command-line tools to test network services.
How to document service verification professionally.

Next Steps:
Explore other common services safely (e.g., HTTP, SSH).
Integrate findings into a cohesive portfolio on GitHub.
