# Lab – Active Directory Group Policy (GPO)

## Daily Ticket
TICKET-AD-001,2026-01-24,Group Policy,User restriction policy request,Created and configured GPO,Applied and verified GPO on client machine,No,Completed
## Objective
This lab demonstrates how to create and apply Group Policy Objects (GPOs) in Active Directory to enforce user and system configurations.

---

## Scenario
An organization requires a security policy to:
- Disable Control Panel access
- Enforce a desktop wallpaper policy

The policy must be applied to all domain users.

---

## Lab Environment
- Windows Server (Domain Controller)
- Windows 10/11 Client VM (Domain Joined)
- Active Directory Domain Services (AD DS)

---

## Step 1: Open Group Policy Management

1. Log into Domain Controller
2. Open:
   Server Manager → Tools → Group Policy Management

Screenshot:
- GPO Management console open

---

## Step 2: Create a New GPO

1. Expand:
   Forest → Domains → YourDomain.local
2. Right-click:
   Group Policy Objects → New
3. Name:
   `User_Restrictions_GPO`

Screenshot:
- New GPO created

---

## Step 3: Edit the GPO

Right-click GPO → Edit

### Disable Control Panel:


 Screenshot:
- Settings configured

---

## 🔹Step 4: Link GPO to OU

1. Right-click your Users OU
2. Click:
   Link an Existing GPO
3. Select:
   User_Restrictions_GPO

📸Screenshot:
- GPO linked to OU

---

## Step 5: Apply Policy on Client Machine

On Windows Client VM:

Open Command Prompt:


📸 Screenshot:
- gpupdate command success

---

## 🔹 Step 6: Verify Policy Applied

Test:
- Try opening Control Panel → Should be blocked
- Desktop wallpaper should change (if configured)

📸 Screenshot:
- Control Panel restriction message

---

## ✅ Outcome
- Successfully created and deployed a GPO
- Enforced user restrictions across domain users
- Verified policy application on client machine

---

## 🧠 Skills Demonstrated
- Active Directory Administration
- Group Policy Management
- Endpoint Configuration
- Domain-Level Policy Enforcement
- Troubleshooting GPO Application

---
