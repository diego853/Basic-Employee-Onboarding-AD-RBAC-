# Basic Employee Onboarding (AD)(RBAC)

## Problem Statement
Northstar Medical Group was managing user access through manual processes with no centralized directory structure. Each department (Finance, HR, IT, Operations) handled access independently, creating inconsistency and security gaps. Users were being granted broad file permissions without proper role-based controls, exposing sensitive patient data and financial records. The lack of organizational structure made it impossible to audit who had access to what. Which is a critical HIPAA compliance requirement. Without a standardized onboarding workflow, access mistakes were inevitable.

## Solution Overview
I built a centralized Active Directory domain (NMG.com) with a structured organizational unit (OU) hierarchy that macthes the company's departments. Each department received its own OU with dedicated security groups, enabling role-based access control (RBAC) where users only access resources required for their job. The new user provisioning starts by adding new hires in their department OU, assigned to the appropriate security group, and immediately inherit the correct file permissions with no manual setup needed.

I demonstrated this by resolving Ticket NMG-0047: Jane Cooper, an HR Payroll Specialist, was placed in the Operations OU and assigned to the operations-users group. This prevented her from accessing HR shared resources and applying the correct desktop policies. I diagnosed the issue by reviewing her OU and security group membership, then moved her to the HR OU and reassigned her to the hr-users group. I verified the fix by reviewing the updated OU structure and security group members list with screenshots. Diagnosing this problem became the blueprint for preventing future access misplacements users in the correct OU automatically inherit the correct permissions.

## Video Walkthrough
[Add your video walkthrough link placeholder here. You will record this tomorrow and update this link so visitors can see a live demonstration of your lab environment.]

## Tools Used
* Windows Server
* Active Directory Domain Services
* VirtualBox
* UTM
* RBAC
* GitHub

## Project Timeline
* Day 1: Domain creation and domain controller promotion
* Day 2: Organizational unit and security group design
* Day 3: User provisioning and RBAC implementation
* Day 4: Incident response and resolution (NMG-0047)
* Day 5: Documentation and case study packaging

## Key Accomplishments
* Built NMG.com domain from scratch
* Probelm solved a mock ticket where a user was given incorrect access
* Simulated a HIPAA-regulated environment by implementing role-based access control and the principle of least privilege.
