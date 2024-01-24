# Microsoft Server 2019 Quick Notes

## Set Static IP Address

- Connect the server to a static IP address

## Change Computer Name
Naming the computer is an ESSENTIAL first step! Do not pass!

- Select "Local Server"
- Select computer name and change it

or...

- Right click windows icon
- Select System
- Select Rename this PC

## Install Active Directory
- Manage
- Add Roles and Features
- Server Roles: Select Active Directory Domain Services (AD DS) and DNS Server (if not already installed)

## Promote to domain controller
- After installing Active Directory Domain Service (AD DS), on the Results page after installation, select "Promote this server to a domain controller" 
- If you exited the Results before promoting, select the notification flag, Find AD DS in notifications and select "Promote this server to a domain controller."
- For this example we are NOT adding the domain to an existing domain or an existing forest, so select "Add new Forest" to create a new Forest.
- Add root Domain name (eg: localserver.local)
- Click “Next” and fill in the necessary details for the Directory Services Restore Mode (DSRM) password, which is used for recovery purposes.
- Follow through the wizard, configuring additional options as needed (DNS, GC, etc.).
- Review your selections and click “Next.”
- The system will perform a prerequisites check. If all checks are passed, click “Install.”
- Server will restart. Note that domain name with your username when logging into the server due to being promoted as a domain controller.


## Join Client PCs to New Domain

IN ORDER for client PC to join domain, you need to enter in the static ip of the server as the DNS server of the client PC.

