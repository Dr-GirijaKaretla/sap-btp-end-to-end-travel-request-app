1. Global Account Setup
Concept:  
A Global Account is the top‑level container for all subaccounts, entitlements, and regions.

Steps:

Log in via SAP BTP Trial/Free Tier.

Select region: Singapore – Azure.

Confirm your global account appears (e.g., 22856012trial).

2. Create Subaccounts (DEV, TEST, PROD)
Concept:  
Each Subaccount is an isolated environment for deployments.

Steps:

Go to Account Explorer → Global Account

Click Create → Subaccount

Enter:

Display Name: DEV / TEST / PROD

Region: Singapore – Azure

Environment: Multi‑Environment

Click Create

Result:  
You now have: DEV, TEST, PROD, and the default trial subaccount.

3. Enable Cloud Foundry in Each Subaccount
Concept:  
Cloud Foundry provides the runtime environment for apps and services.

Steps:

Open subaccount → Cloud Foundry

Click Enable Cloud Foundry

Keep defaults:

Environment: Cloud Foundry Runtime

Plan: trial

Instance Name: auto‑generated or rename (DEV_CF, TEST_CF, PROD_CF)

Org Name: keep auto‑generated

Click Create

4. Create Spaces (dev, test, prod)
Concept:  
A Space is a logical deployment area inside a Cloud Foundry org.

Steps:

Subaccount → Cloud Foundry → Spaces

Click Create Space

Enter:

DEV → dev

TEST → test

PROD → prod

Save

5. Entitlements – Understanding & Confirmation
5.1 Concept
Entitlements determine which services each subaccount is allowed to use.

There are two levels:

A. Global Account Level – Configure Entitlements
This is where you add service plans to the global account so they become available to subaccounts.

Important:  
The Configure Entitlements button appears ONLY at:

Global Account → Entitlements  
(not inside subaccounts)

B. Subaccount Level – Entitlements Tab
This is where you see which services are already assigned to that subaccount.

5.2 Required Services for This Project
These services must appear under each subaccount’s Entitlements tab:

Cloud Foundry Environment (trial)

Destination Service (lite)

Connectivity Service (lite)

HTML5 Application Repository (app-host, app-runtime)

Application Autoscaler (standard)

Cloud Identity Services (application)

Service Manager roles (auto‑assigned)

5.3 Confirmation
Your DEV subaccount already shows all required services.
This confirms that entitlements are correctly assigned even if the Configure Entitlements button was not visible.

6. Default “trial” Subaccount
Auto‑created by SAP

Contains a default Cloud Foundry org/space

Safe to keep for now

Can delete later once DEV/TEST/PROD are stable

✔ Day 1 Completed Successfully
By the end of Day 1, you have:

Global Account: 22856012trial

Subaccounts: DEV, TEST, PROD, trial

Cloud Foundry enabled in DEV/TEST/PROD

Spaces created: dev, test, prod

Entitlements confirmed and visible in DEV (and will appear similarly in TEST/PROD)
