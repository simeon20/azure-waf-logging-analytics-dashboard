# azure-waf-logging-analytics-dashboard
Built a custom Azure WAF monitoring solution leveraging Log Analytics, Workbooks, and dashboards to visualize web traffic and security events.
---
This project demonstrates how to set up Azure Application Gateway with Web Application Firewall (WAF) and integrate it with Log Analytics, Workbooks, and Dashboards for monitoring real-world web traffic and security events.

---

![Dashboard Screenshot](MyDashboard.png)

---

🚀 Project Overview

Built a custom Azure WAF monitoring solution leveraging:

Deployable ARM template for Azure Application Gateway (WAF v2) with built-in traffic inspection and protection.

Log Analytics Workspace to collect and query diagnostic logs.

Workbooks & Dashboards to visualize key metrics such as:

Top targeted URLs

Top client IPs

Allowed vs. blocked requests

Top 10 WAF rules triggered

Blocked requests over time

---
Getting Started<br>
<br>
Step 1.
Deployable ARM template for Azure Application Gateway (WAF v2) with built-in traffic inspection and protection and assocate/add a WAF Policy.
[View the ARM Template](azure-application-gateway-arm-template)
<br>
<br>
1. Go to the Azure Portal → Create a resource → search “Template deployment (deploy using custom templates)” → Create.

2. On Custom deployment, choose Build your own template in the editor → Load file → upload your template.json.

3. Click Save.

4. Fill in:

        Subscription, Resource group (create one if needed).

        Region (must match or be valid for AGW).

        Parameters (paste External IDs or use the defaults if you left placeholders).

5. Review + create → Create.

6. Watch notifications for deployment status; click the Deployment to see details.

Post-deploy checks (Portal):

  Resource Group → Application Gateways → select your gateway. Confirm:

        Status = Running

        Frontend public IP is assigned

        Backend health shows Healthy for the probe

        WAF policy is attached
        <br>
WAP Policy
![WAF Screenshot](WAFPolicy.png)

