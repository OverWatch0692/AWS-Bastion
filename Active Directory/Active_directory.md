1. Installing Active Directory Domain Services (AD DS)

Active Directory Domain Services is a server role that allows you to create a new domain or join an existing one, enabling centralized management of network resources.

a. Prerequisites:

Operating System: Ensure you're using a Windows Server edition that supports AD DS (e.g., Windows Server 2016 or later).

Static IP Address: Assign a static IP address to the server to ensure consistent network identification.

b. Steps to Install AD DS:

Open Server Manager:

Log in to the Windows Server.

Click on the Start menu, then select Server Manager.

Add Roles and Features:

In Server Manager, click on Manage > Add Roles and Features.

Proceed through the Before You Begin page by clicking Next.

Select Installation Type:

Choose Role-based or feature-based installation and click Next.
Select Destination Server:

Ensure your server is selected from the server pool and click Next.
Select Server Roles:

Check the box for Active Directory Domain Services.

A pop-up will appear to add required features; click Add Features.

Click Next.

Add Features:

No additional features are needed for AD DS; click Next.
AD DS Overview:

Review the information provided and click Next.
Confirm Installation Selections:

Optionally, check Restart the destination server automatically if required.

Click Install.

Complete Installation:

Once the installation is complete, click Close.
c. Promote Server to Domain Controller:

Post-Deployment Configuration:

In Server Manager, a notification flag will indicate Post-deployment Configuration is needed.

Click on Promote this server to a domain controller.

Deployment Configuration:

Choose Add a new forest if creating a new domain.

Enter the Root domain name (e.g., example.local).

Click Next.

Domain Controller Options:

Select the Forest functional level and Domain functional level (e.g., Windows Server 2016).

Ensure Domain Name System (DNS) server is checked.

Set a Directory Services Restore Mode (DSRM) password.

Click Next.

DNS Options:

If a delegation for this DNS server cannot be created, you may see a warning; this can be ignored in a new forest setup.

Click Next.

Additional Options:

The NetBIOS domain name will be auto-filled based on your domain name.

Click Next.

Paths:

Specify locations for the Database, Log files, and SYSVOL folders or accept defaults.

Click Next.

Review Options:

Review your selections and click Next.
Prerequisites Check:

The system will perform checks; ensure all prerequisites are met.

Click Install.

Completion:

The server will restart upon completion.
2. Creating and Applying Group Policy Objects (GPOs)

Group Policy allows administrators to define configurations for both users and computers within the domain, providing centralized management and configuration of operating systems, applications, and user settings.

a. Open Group Policy Management Console (GPMC):

Log in to a server or workstation with GPMC installed.

Navigate to Start > Administrative Tools > Group Policy Management.

b. Create a New GPO:

In the GPMC console, expand your domain (e.g., example.local).

Right-click on the Group Policy Objects container and select New.

Enter a Name for the GPO (e.g., "Password Policy") and click OK.

c. Edit the GPO:

Right-click the newly created GPO and select Edit.

The Group Policy Management Editor will open.

Navigate to the desired configuration path:

For Computer Configuration: Policies > Administrative Templates > [Policy Path]

For User Configuration: Policies > Administrative Templates > [Policy Path]

Double-click the policy setting you wish to configure, set it as Enabled or Disabled, and configure any additional options.

Click Apply, then OK
