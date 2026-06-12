# Active-Directory-Home-Lab
Walkthrough and documentation of my Windows Server 2022 and Active Directory home lab.
## Purpose and Technologies Used
* **Purpose:** To build a fully functional Active Directory environment from scratch to practice enterprise user management, group policies, and core networking concepts.
* **Operating Systems:** Windows Server 2022, Windows 11
* **Hypervisor:** Oracle VirtualBox

## Project Steps
1. Hypervisor and Virtual Network Configuration
2. Windows Server 2022 Installation and IP Configuration
3. Active Directory Domain Services (AD DS) Promotion
4. Creating Organizational Units (OUs) and Users
5. Joining a Windows 11 Client to the Domain
6. Group Policy Object (GPO) Implementation

---

## Project Walkthrough

### 1. Domain Infrastructure & DNS Health
* **Objective:** To build and secure a functional enterprise domain using Oracle VirtualBox to practice Tier 1 IT Support skills.
* **Action:** Verified the health of Active Directory Integrated DNS zones. This ensures the domain can correctly resolve names, which is critical for workstations to locate the Domain Controller.

#### Verification Screenshot:
<img width="752" height="520" alt="Lab_DNS_Health_Check" src="https://github.com/user-attachments/assets/99a9c6ec-cca7-4eeb-a9e9-f324b101eb90" />
### 2. Network Connectivity & IP Configuration

#### Static IP & DNS Verification:
<img width="955" height="506" alt="Network_IP_Configuration_Verification" src="https://github.com/user-attachments/assets/8e8508fc-07bb-4b25-97ea-b5fbb9c3caea" />
<img width="964" height="508" alt="Network_IP_Configuration_Verification2" src="https://github.com/user-attachments/assets/7f1c8430-fe94-4942-bd40-c831cd701d0b" />
* **Action:** Verified the network ‘handshake’ by confirming the Server is set to a Static IP and the Windows 11 workstation is correctly pointing to that IP for DNS resolution. This configuration is essential for the client to authenticate with the Active Directory domain.

#### Connectivity & Loopback Diagnostics:
* **Diagnostics:** Performed a Ping test to the Domain Controller to verify network communication and a Loopback test to confirm the local TCP/IP stack was functioning correctly.
<img width="996" height="622" alt="Loopback_Test_NIC" src="https://github.com/user-attachments/assets/4a54036e-c13d-4123-ac5b-d2e72ec7b103" />
<img width="996" height="620" alt="Ping_Server_Connectivity" src="https://github.com/user-attachments/assets/c42ebbd7-9fcd-42da-b4d5-904d91714f6f" />
