
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

# osTicket - Post-Installation Configuration
This documentation outlines the post-installation configurations for the osTicket help desk ticketing system. These steps ensure the system is tailored to the organization's needs, enabling efficient support management and role-based access.

osTicket is an open-source ticketing solution that centralizes support requests and automates workflows. This guide demonstrates the configuration of roles, departments, agents, users, SLAs, and help topics, along with a distinction between agent and admin panels.

---

## Table of Contents
1. [Access Points](#access-points)
2. [Post-Installation Configuration Steps](#post-installation-configuration-steps)
    - [Login Pages](#login-pages)
    - [Roles and Permissions](#roles-and-permissions)
    - [Departments and Teams](#departments-and-teams)
    - [User and Agent Configuration](#user-and-agent-configuration)
    - [SLA Management](#sla-management)
    - [Help Topics](#help-topics)
3. [Troubleshooting](#troubleshooting)
4. [Licensing Information](#licensing-information)
5. [Contact Information](#contact-information)

---

## Access Points

- **Admin/Analyst Login Page**: [http://localhost/osTicket/scp/login.php](http://localhost/osTicket/scp/login.php)  
- **End Users osTicket URL**: [http://localhost/osTicket](http://localhost/osTicket)  

---

## Post-Installation Configuration Steps

### Login Pages
- Understand the difference between the **Agent Panel** and the **Admin Panel**:
  - **Agent Panel**: Where support agents manage tickets and interact with users.
  - **Admin Panel**: Where administrators configure system settings, roles, departments, and more.

### Roles and Permissions
- Configure roles to group permissions logically:
  1. Navigate to **Admin Panel -> Agents -> Roles**.
  2. Create a role named **Supreme Admin** for unrestricted access.

### Departments and Teams
- Define departments for ticket visibility and segmentation:
  1. Go to **Admin Panel -> Agents -> Departments**.
  2. Add a department named **SysAdmins**.

- Create cross-department teams to collaborate on specific tasks:
  1. Navigate to **Admin Panel -> Agents -> Teams**.
  2. Create a team called **Online Banking**.

### User and Agent Configuration
- Allow unregistered users to create tickets or require registration:
  1. Navigate to **Admin Panel -> Settings -> User Settings**.
  2. Uncheck **"Unregistered users can create tickets"** to require registration and login.

- Add agents to manage tickets:
  1. Go to **Admin Panel -> Agents -> Add New**.
  2. Add the following agents:
     - **Jane** (Department: SysAdmins)
     - **John** (Department: Support)

- Add customers as users for ticket creation:
  1. Navigate to **Agent Panel -> Users -> Add New**.
  2. Add the following users:
     - **Karen**
     - **Ken**

### SLA Management
- Configure SLAs (Service Level Agreements) to set ticket resolution time expectations:
  1. Navigate to **Admin Panel -> Manage -> SLA**.
  2. Add the following SLAs:
     - **Sev-A**: Grace Period - 1 hour, Schedule - 24/7.
     - **Sev-B**: Grace Period - 4 hours, Schedule - 24/7.
     - **Sev-C**: Grace Period - 8 hours, Schedule - Business Hours.

### Help Topics
- Define help topics to categorize user tickets efficiently:
  1. Go to **Admin Panel -> Manage -> Help Topics**.
  2. Add the following topics:
     - **Business Critical Outage**
     - **Personal Computer Issues**
     - **Equipment Request**
     - **Password Reset**
     - **Other**

---

## Troubleshooting

1. **Issue**: Users are unable to create tickets despite registration being enabled.  
   - **Cause**: Incorrect settings under **User Settings**.  
   - **Solution**: Verify that the **"Require registration and login to create tickets"** option is unchecked.

2. **Issue**: Agents cannot view tickets assigned to their department.  
   - **Cause**: Incorrect role or department assignment.  
   - **Solution**: Ensure the agent's role and department align with their ticket visibility requirements.

3. **Issue**: SLA grace periods are not being enforced.  
   - **Cause**: SLA policies are not applied to tickets.  
   - **Solution**: Confirm that the correct SLA is selected during ticket creation.

---

## Licensing Information
osTicket is distributed under the GNU General Public License (GPL). For more information, visit the [osTicket License](https://osticket.com).

---

## Contact Information
For questions or feedback, feel free to reach out:  
- **GitHub**: https://github.com/Pieratboi  
- **LinkedIn**: <a href="https://www.linkedin.com/in/rafael-razapov-60391a2b8/?trk=opento_sprofile_topcard"> Rafael Razapov </a>  
