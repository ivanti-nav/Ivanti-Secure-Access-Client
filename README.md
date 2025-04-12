# Download Ivanti Secure Access Client

The Ivanti Secure Access Client provides a dependable and secure remote access solution, allowing users to connect seamlessly and in line with enterprise guidelines to internal systems. It guarantees that individuals—no matter where they are—can securely reach company applications, servers, and file repositories without compromising cybersecurity.

## Table of Contents

- [Installation](#installation)  
- [User Roles and Access Control](#user-roles-and-access-control)  
- [Authentication and Security Policies](#authentication-and-security-policies)  
- [Single Sign-On (SSO) and Adaptive Authentication](#single-sign-on-sso-and-adaptive-authentication)  
- [Host Checker and Endpoint Security](#host-checker-and-endpoint-security)  
- [VPN Tunneling and Secure Application Manager](#vpn-tunneling-and-secure-application-manager)  

## Installation

**[Download Ivanti Secure Access Client](*)**  

After downloading the Ivanti Secure Access Client, follow these steps to install and configure it:

- Run the installer and follow the on-screen instructions to complete setup.  
- Log in with your enterprise credentials.  
- Configure VPN settings according to your organization’s security requirements.  
- Establish a secure connection to access internal resources safely.  

If needed, refer to your IT department or consult the official Ivanti documentation for more detailed guidance.

---

## User Roles and Access Control

### Understanding User Roles
User roles define the permissions assigned to various user groups in ICS. Administrators can create roles that govern access to resources, session settings, and interface behavior.

### Role-Based Access Management
ICS supports two primary types of roles:
- **Administrator Roles:** Provide full administrative privileges within the ICS platform.  
- **User Roles:** Determine session characteristics, access rights, and available features for regular users.  

#### Creating a New User Role
```plaintext
1. Navigate to Users > User Roles in the admin console.
2. Click "New Role" and assign a name.
3. Define session policies and access levels.
4. Save the role and associate it with the relevant authentication realms.
```

---

## Authentication and Security Policies

### Authentication Methods
ICS integrates with several types of authentication servers to confirm user identity, including:

- **Local Authentication Server**  
- **Active Directory (AD)**  
- **LDAP**  
- **RADIUS**  
- **SAML-based systems**  

### Setting Up Authentication Realms
Authentication realms describe how users are authenticated and mapped to roles.

#### Configuration Steps
1. Go to **Users > Authentication > User Realms**.  
2. Click **New Realm** and enter a unique name.  
3. Select the desired authentication server.  
4. Set up user validation and role-mapping rules.  
5. Save the configuration and link the realm to a sign-in policy.  

> **[!info]**  
> Enabling multi-factor authentication (MFA) is highly recommended for enhanced protection.

---

## Single Sign-On (SSO) and Adaptive Authentication

### Configuring SSO
Single Sign-On (SSO) lets users log in once and access multiple applications without repeated authentication.

ICS supports the following SSO options:
- **SAML 2.0 for web-based SSO**  
- **NTLM authentication**  
- **Kerberos protocol**  

#### Enabling SSO
```plaintext
1. Go to Authentication > Single Sign-On.
2. Select your preferred protocol (SAML, NTLM, or Kerberos).
3. Enter the identity provider configuration.
4. Associate the SSO setup with relevant authentication realms.
5. Save and validate the login process.
```

### Adaptive Authentication
Adaptive authentication evaluates the context—such as user behavior, device characteristics, and location—to decide on access rights.

#### Implementation Steps
- Establish risk profiles based on device status, IP address, and behavioral patterns.  
- Define rules that scale authentication requirements depending on risk assessment.

---

## Host Checker and Endpoint Security

**Host Checker** functions as a compliance scanner, verifying that the connecting device adheres to predefined security standards before granting access.

### Configuring Host Checker Policies
1. Go to **Authentication > Host Checker**.  
2. Create a policy outlining the compliance requirements (e.g., antivirus, firewall settings, OS patch level).  
3. Assign the policy to specific authentication realms.  
4. Configure actions for devices that do not meet the criteria.

> **[!note]**  
> Regularly update Host Checker policies to address new and evolving threats.

---

## VPN Tunneling and Secure Application Manager

### VPN Tunneling
ICS leverages **SSL-based VPN tunneling** to deliver full Layer 3 network access to internal corporate systems.

#### Configuration Steps
- Go to **Users > User Roles** and enable **VPN Tunneling**.  
- Define routing parameters and enable split tunneling if necessary.  
- Apply policies for controlling session time limits and bandwidth usage.

### Secure Application Manager (SAM)
SAM provides secure access to application-level traffic used by client-server applications.

#### Enabling SAM
- Open **Users > User Roles > Secure Application Manager**.  
- Set the allowed services and define server destinations.  
- Assign access policies based on the user role.

---

## Resource Policies and Access Control

Resource policies regulate how users access **web-based applications, shared files, and internal systems**.

### Creating Resource Policies
1. Navigate to **Users > Resource Policies**.  
2. Select the appropriate resource type (Web, File, Terminal Services, etc.).  
3. Specify allowed or restricted resources.  
4. Link the policy to relevant user roles.

> **[!important]**  
> Conduct regular audits of resource policies to ensure they align with security standards.

---

## Logging, Monitoring, and Troubleshooting

### Logging and Event Monitoring
ICS comes with **robust tools for logging and real-time monitoring**.

- Enable logging via **System > Logging**.  
- Use **Syslog** to forward logs to external monitoring solutions.  
- Leverage **Admin Console diagnostics** for active issue tracking.

### Troubleshooting Common Issues
- **Login errors:** Check your authentication server configurations and network connectivity.  
- **VPN connectivity problems:** Review firewall rules and VPN settings.  
- **Performance lags:** Monitor system load and consider implementing load-balancing strategies.

---

## Clustering and High Availability

### Configuring Clustering
ICS allows for **clustering** to support fault tolerance and balanced traffic distribution.

#### Setup Steps
1. Go to **System > Clustering**.  
2. Add additional nodes and configure synchronization settings.  
3. Select either **active/passive** or **active/active** clustering modes.

---

## System Maintenance and Configuration Backup

### Performing System Updates
Keeping the system updated is essential for **security and system stability**.

#### Updating ICS
1. Go to **Maintenance > System Update**.  
2. Upload the latest firmware file.  
3. Reboot the system to apply the update.

### Backing Up Configuration Files
Backing up configuration data ensures protection against accidental loss or misconfiguration.

#### Backup Process
- Head to **Maintenance > Configuration Backup**.  
- Click **Export Configuration**.  
- Store the backup in a **secure and retrievable location**.

> **[!note]**  
> Use scheduled backups to minimize manual effort and ensure consistency.
