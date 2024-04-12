# Setting-up-a-honeypot-to-detech-and-analyze-cyber-threats

## Overview of a Honeypot
• A honeypot is a computer security mechanism to identify, block or counteract attempts at unauthorized use of information systems. 

• They serve as early warning systems, providing insights into the tactics, techniques, and procedures (TTPs) of cyber attackers.

• There are two kinds of honeypots, including low-interaction and high-interaction honeypots, each with its own level of complexity and resource requirements.


## Steps to setup a honeypot
### 1. Deploying a new server to interact with the honeypot on a cloud provider
   I have used [Vultr](https://my.vultr.com/welcome/) as my cloud provider to deploy a new server.
<img width="1512" alt="Screenshot 2024-04-12 at 4 52 48 PM" src="https://github.com/Avikaj/Setting-up-a-honeypot-to-detech-and-analyze-cyber-threats/assets/151662350/66740d87-0a4d-4e1b-8a66-057c6a61d77a">

 along with the [T-pot ISO Image](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqa29aRjJheWVfbHdZWjdfaVRKZ0E2Z25FLVJzUXxBQ3Jtc0tsQUt5ZHFJMHpPeVRXR19uMkIyUlRhdjg4T1k0RVltM1FIOVVxeGFjbklZSFI5b19FWjRPWVlsQUdWWTRxdG9SdThvd2NsNnFfeTV1eGFXelp6Q1V6MXB4V190YTFJb1ZXVFV4X0M4R1I4VFBCaHNINA&q=https%3A%2F%2Fgithub.com%2Ftelekom-security%2Ftpotce%2Freleases%2Fdownload%2F22.04.0%2Ftpot_amd64.iso&v=FtR9sFJlkSA) and a firewall (first so that only we can access it, to finish configuring and then so that the internet has the access).

 <img width="1512" alt="Screenshot 2024-04-12 at 5 03 52 PM" src="https://github.com/Avikaj/Setting-up-a-honeypot-to-detech-and-analyze-cyber-threats/assets/151662350/cb41db78-2397-4ab6-93e5-c33e9abd9f9a">


### 2. Installing t-pot  on Debian GNU/Linux 

• Debian GNU/Linux is used to enable flexible and reliable deployment for capturing malicious activity.
<img width="1467" alt="Screenshot 2024-04-12 at 5 09 48 PM" src="https://github.com/Avikaj/Setting-up-a-honeypot-to-detech-and-analyze-cyber-threats/assets/151662350/5e28a85e-a5bb-4007-b9c3-d31c48506735">

### 3. Getting to the T-pot console

• Using the address of the t-pot provided to us in Step 2, we get to the t-pot console
<img width="1510" alt="Screenshot 2024-04-12 at 5 11 13 PM" src="https://github.com/Avikaj/Setting-up-a-honeypot-to-detech-and-analyze-cyber-threats/assets/151662350/089f173d-3fb7-4518-bea6-524365b3ea4b">

Here, we can use a variety of services provided bt t-pot:

a. *Attack Map* provides a animated attack map to analyze the incoming attack countries, IP addresses etc.

b. *Cockpit* for web based remote access, management and web terminal.

c. *CyberChef* a web app for encryption, encoding, compression and data analysis.

d. *Elasticvue* a web front end for browsing and interacting with an Elasticsearch cluster.

e. *Kibana* for displaying events on beautifully rendered dashboards.

f. *Spiderfoot* an open source intelligence automation tool.



### 4. Making the honeypot accessible to the internet

This was the view of attacks on the Attack Map after 30 minutes of making the honeypot vulnerable.

![Screenshot 2024-04-12 at 5 35 36 PM](https://github.com/Avikaj/Setting-up-a-honeypot-to-detech-and-analyze-cyber-threats/assets/151662350/aea72b63-5c24-463b-a606-a90eb3b2176c)




This is the Elasticvue of the "Honeytrap" honeypot that was used to attack this hoenypot.

It includes the total number of attacks, the number of unique source IPs, charts displaying attacks by port numbers, attacks by countries etc.


<img width="1511" alt="Screenshot 2024-04-12 at 5 28 53 PM" src="https://github.com/Avikaj/Setting-up-a-honeypot-to-detech-and-analyze-cyber-threats/assets/151662350/5eef6492-7497-4672-81e5-e217bf8e6d1c">


