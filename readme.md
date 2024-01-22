# Microsoft Server 2019 Quick Notes

## Change Computer Name
- Select "Local Server"
- Select computer name and change it

## Install Active Directory
- Manage
- Add Roles and Features
- Server Roles: Select all Active Directory Items (AD Cert)

## Promote to domain controller
- After installing Active Directory Domain Service (AD DS), select Flag notification
- Find AD DS in notifications and select "Promote this server to a domain controller."
- Select "Add new Forest"
- Add root Domain name
- Click “Next” and fill in the necessary details for the Directory Services Restore Mode (DSRM) password, which is used for recovery purposes.
- Follow through the wizard, configuring additional options as needed (DNS, GC, etc.).
- Review your selections and click “Next.”
- The system will perform a prerequisites check. If all checks are passed, click “Install.”

If you receive a "Verification of prerequities for Domain Controller promotion failed. Certificate server is installed." Error:

Remove the AD CS Role (if applicable):

- Open Server Manager.
- Go to Manage > Remove Roles and Features.
- Deselect Active Directory Certificate Services from the roles list.
- Follow the prompts to complete the removal process.
- Restart the server.
