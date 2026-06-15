# Active Directory Lab: Simulating Real IT Support Scenarios

This project simulates common Tier 1 IT support tasks in a Windows Active Directory environment, including user management, domain configuration, and troubleshooting real-world issues.

---

### Project Overview
* DNS configuration and domain connectivity
* Domain-joined client setup and validation
* Active Directory user and group management
* Troubleshooting login failures and account lockouts
* Basic IT support workflows in a Windows environment

---

### Technologies Used
* **Operating Systems:** Windows Server 2022, Windows 11
* **Hypervisor:** Oracle VirtualBox
* **Core Services:** Active Directory Domain Services (AD DS), DNS

---

### Lab Environment Architecture
To simulate an enterprise environment, the lab was built using a private virtual network with the following specifications:
* **Domain Controller:** Windows Server 2022, configured as a root domain controller.
* **Network Configuration:** Configured with an isolated virtual network adapter to manage lab traffic and ensure secure internal communication.
* **Client Workstation:** Windows 11, deployed on the same virtual network to test end-user policies and help desk troubleshooting.

---

## Project Walkthrough & Documentation

### 1. Network Infrastructure & Connectivity
* **Objective:** Establish the foundation of the lab by configuring static IP addressing and verifying network communication between the Client and the Domain Controller.

**Static IP & DNS Verification:**
* **Action:** Verified the network ‘handshake’ by confirming the Server is set to a Static IP and the Windows 11 workstation is correctly pointing to that IP for DNS resolution.

<img width="955" height="506" alt="Network_IP_Configuration_Verification" src="https://github.com/user-attachments/assets/8e8508fc-07bb-4b25-97ea-b5fbb9c3caea" />
<img width="964" height="508" alt="Network_IP_Configuration_Verification2" src="https://github.com/user-attachments/assets/7f1c8430-fe94-4942-bd40-c831cd701d0b" />

**Connectivity & Loopback Diagnostics:**
* **Diagnostics:** Performed a Ping test to the Domain Controller to verify network communication and a Loopback test to confirm the local TCP/IP stack was functioning correctly.
<img width="996" height="622" alt="Loopback_Test_NIC" src="https://github.com/user-attachments/assets/4a54036e-c13d-4123-ac5b-d2e72ec7b103" />
<img width="996" height="620" alt="Ping_Server_Connectivity" src="https://github.com/user-attachments/assets/c42ebbd7-9fcd-42da-b4d5-904d91714f6f" />

**Domain Infrastructure & DNS Health:**
* **Action:** Verified the health of Active Directory Integrated DNS zones to ensure proper name resolution across the domain.
<img width="752" height="520" alt="Lab_DNS_Health_Check" src="https://github.com/user-attachments/assets/99a9c6ec-cca7-4eeb-a9e9-f324b101eb90" />

---

### 2. Identity & Access Management (Active Directory)
* **Objective:** To establish a structured and secure identity management framework by implementing Organizational Units (OUs) and provisioning user accounts.
* **Action:** Configured the logical structure of the domain by creating dedicated Organizational Units (OUs) for business departments (Marketing and Sales) and provisioned standard user accounts to simulate enterprise identity management.

**Active Directory Users and Computers (OU & User Provisioning):**
<img width="752" height="527" alt="AD_Sales_OU_JamesMiller" src="https://github.com/user-attachments/assets/d0494f1c-e505-475a-9f5b-19d885aa47e3" />

---

### 3. Incident Remediation & Help Desk Scenarios
* **Objective:** Simulate real-world Tier 1 support tickets, including account lockouts, password resets, and permission enforcement.

* **Scenario A (Account Lockout):** Implemented a GPO-based Account Lockout Policy, monitored user authentication errors, and demonstrated administrative remediation by unlocking the account.
<img width="1023" height="693" alt="Client_Account_Lockout_Error" src="https://github.com/user-attachments/assets/7e830ae7-484b-4aef-9c98-c2402c3ad1aa" />
<img width="411" height="553" alt="AD_Account_Unlock_Admin" src="https://github.com/user-attachments/assets/762b4a5b-7173-445c-87d7-3c7885c3389e" />

* **Scenario B (Password Reset):** Demonstrated the process of successfully executing an administrative password reset within Active Directory Users and Computers to restore user access.
<img width="755" height="531" alt="AD_Password_Reset_Success" src="https://github.com/user-attachments/assets/ece7b0e5-c7f1-4c0c-90d7-9855ef5ff71e" /> 

* **Scenario C (Access Control Validation):** Implemented security settings enforcing the Principle of Least Privilege (PoLP). Successfully restricted access to the "Marketing_Data" share and verified that unauthorized users were correctly blocked.
<img width="783" height="594" alt="Sarah_Access_Denied" src="https://github.com/user-attachments/assets/783c1fd4-207e-4f20-a130-966d442a392d" />

---

### Key Takeaways
* Gained hands-on experience with Active Directory infrastructure in an enterprise-simulated environment.
* Developed systematic troubleshooting methodologies for common network, DNS, and user account issues.
* Built foundational knowledge of Windows Server administration, Group Policy Objects (GPOs), and network security mapping.
