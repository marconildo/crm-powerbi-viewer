---
layout: page
title: Add a Power BI View
tagline: to Dynamics 365
description: How to add a view from Power BI to a dashboard in Dynamics 365 Sales and Service.
---

You embed a Power BI view by referencing the Power BI element id. If you, as recommended, embed views from a group workspace you also need to reference the group id.

The easiest approach to find elements you have access to and the required CRM configuration is by going to the solution
configuration page.

The configuration page lists available reports, dashboards and tiles. Both those you have access to through your personal workspace and those through
group membership(s). Click preview to see how the view looks inside Dynamics 365 (note: previews are shown inside the configuration page).

   > [![]({{BASE_PATH}}/assets/images/v1.0/crm-config/config-overview.png)]({{BASE_PATH}}/assets/images/v1.0/crm-config/config-overview.png)
<br />
<br />

**On-premise and using Edge?** The security in Edge prevents communication between the webresource and the authentication popup if they are not in the same security zone
You have two options; 1: Add "https://login.microsoftonline.com" to the same zone as your CRM instance, or 2: Disable protected mode on the security zone. This must be
changed for all users.
{: .alert .alert-warning }

## Steps
The following example uses a report, but the exact same procedure applies to dashboard and tiles.

1. When you have found the report you want to use you need to copy the configuration values. Click the clipboard icon to copy the configuration values to the clipboard. 

   > [![]({{BASE_PATH}}/assets/images/v1.0/crm-config/config-copy2clipboard-report.png)]({{BASE_PATH}}/assets/images/v1.0/crm-config/config-copy2clipboard-report.png)

2. Next create a new dashboard and add the web resource named **'his_/powerbi/viewer.html'**.
3. Give the resource a meaningful name and label.
4. Paste the configuration from step 1 into *'Custom parameter (data)'*.

   > [![]({{BASE_PATH}}/assets/images/v1.0/crm-config/config-add-webresource-report.png)]({{BASE_PATH}}/assets/images/v1.0/crm-config/config-add-webresource-report.png)

5. Save and publish the dashboard.
6. You are done! The result should be similar to the image below.

<br />
   > [![]({{BASE_PATH}}/assets/images/v1.0/samples/sample-report-dashboard-salesperf.png)]({{BASE_PATH}}/assets/images/v1.0/samples/sample-report-dashboard-salesperf.png)

<br />
<br />
<br />
 

### The parameter constructs are:

Remove **groupid** including brackets when embedding a personal view.

#### Report
```
type=report&id=<reportid>[&groupId=<groupId>]&pageName=[initialPage]&showFilterPane=true&showNavPane=true
```

#### Dashboard
```
type=dashboard&id=<dashboardid>[&groupId=<groupId>]
```

#### Tile
```
type=tile&id=<tileid>&dashboardId=<dashboardid>[&groupId=<groupId>]
```
