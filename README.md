# Ultimate-SOC-LAB
H0L@ guys, the main question is why this lab. I would be straightforward.
* Dont worry none of the words is AI generative
1. To show my skills, knowledge and experience that is of interest i.e SOC Analyst
2. Exploring the different tools required in the Blue team so that you can learn more about the Red/Purple team while on the job.
3. Contributing to get a job without certifications in the Industry which is quite hard, and I have never chosen an easy path.
   !<img src="https://github.com/user-attachments/assets/9d361b5f-e9c4-4133-af63-6b2d7cc5e467" ><br /> Image 1. This is where we are heading it's a never-ending process so bear with me!


## Phase 1 Proxmox 8.1.4 PVE 
1. Find the Hardware
   - I am using the Acer Aspire XC-885 series given the below specification
   
       <img src="https://github.com/mark-nirdesh/Ultimate-SOC--LAB/assets/53371402/4e5d38f9-ff4a-43e0-aefa-0cacf46e1a07" width="500px"><br /> 
       Image 1.1 screenshot from the Dashboard of Proxmox running PVE
2.  Download [Proxmox](https://www.proxmox.com/en/downloads/proxmox-virtual-environment/iso) iso file latest(8.1.4)
3.  Make USB bootable with your favourite bootable software- [RUFUS](https://rufus.ie/en/)
4.  Boot from USB and Install Proxmox.(basic installation is not covered just important parts covered)
5.  Install it like Linux OS and it will be available  on  machine.IP-address:8006
   
## Phase 2 
1. Download the ISO images and Upload them to the Proxmox hard drive.
   <img src="https://github.com/user-attachments/assets/7daae5dd-74d8-4118-9497-35bfb2d10c0e" width="500px"><br /> Image 2.1 screenshot from the ISO images on Proxmox Storage
   -  pfsense firewall https://www.pfsense.org/download/
   -  Ubuntu Server https://ubuntu.com/download/server
   -  Kali Linux https://www.kali.org/get-kali/#kali-platforms
   -  Parraot OS https://parrotsec.org/download/

2. Configure the Linux Bridge.<br />
    <img src="https://github.com/user-attachments/assets/036377f8-04f7-4f9c-b5d2-53495dd3fa23" width="500px"><br /> Image 2.2  You can choose your private IP range* try your networking skills!
## Phase 3 pfsense firewall 
   - install pfsense firewall ISO with Network adapter as Linux bridge
   - we can access the firewall with CLI and WEB_GUI= ip.address
   - Create Interfaces for VLANs vlan10, vlan20, vlan30
   - Create firewall rules for each VLAN <br /><img src="https://github.com/user-attachments/assets/bd004fc3-9dc8-46d0-a809-488a187ebdf7" width="500px"><br />
   - Enable DHCP for each VLANs you can choose your IP range(* try  your subnetting skills)
## Phase 4 Install Kali, Parrot OS, and Ubuntu Server at  your desired VLANs
-  Keep Updated with the latest updates make it personalize and remember all the passwords and usernames.
-  try pinging from each machine to check connectivity.
-  Install  WAZUH(SIEM + EDR) from here https://documentation.wazuh.com/current/quickstart.html on a Headless Ubuntu Server by SSH  
-  install Nessus(Vuneralibity Scanner) from here https://www.tenable.com/downloads/nessus?loginAttempted=true on a Headless Ubuntu Server by SSH
-  install Splunk Enterprise(SIEM) from here https://www.splunk.com/en_us/download/splunk-enterprise.html?locale=en_us# (need login ID) 
## Phase 4 Create VM with Vulnerable machine from Vulnhub.com at your honey pot VLAN
1. You can choose your machine as you want
- You can try solving this box , This will give you peneration testing hands-on with privlage escalation, finding vulneralibities by open ports and services on that particilar machine
   <br />-> I choose 5 machines as follows<br />Machine 5: Breakout <br /> Machine 4: Metasploitable-linux-2.0.0 <br /> Machine 3: ICA1 <br />Machine 2: Earth <br /> Machine 1: Matrix

## Phase 5 Setting up sensor or agents to get telemtry or logs on SIEM i.e. splunk or Wazuh
- We can't start penetration testing on the box as we havent setup the agents on the machine
- As we don't know the username and password we cant login and get setup the agents or sensor or forwarder.
- so what we can do? think about it and then get to here for next step.
       

  
