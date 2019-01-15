---
layout: page
title: CRM Power BI Viewer
tagline: add the Power of BI to Dynamics 365
description: Embed Power BI reports/tiles into Dynamics CRM dashboards and forms.
---
**Improved Power BI integration coming...?**<br/>
Recent [communication](https://docs.microsoft.com/en-us/business-applications-release-notes/october18/powerapps/power-bi-embedding-available-in-common-data-service-entity-forms) and rumors
hints of improved support for Power BI to be expected in the coming v10 of CE. Fingers crossed...<br/><br/>
The future of CRM Power BI Viewer depends on what Power BI support Microsoft actually releases with v10. Additionally Microsoft has yet to release documentation
on how to create custom controls for their new user interface. The consequence being that it is not possible to develop a proper CRM Power BI Viewer for v9 and above...<br/><br/>
This project is not dead, but further development is postponed until more is known about the coming release of CE Q1 2019.
{: .alert .alert-error }

[Download](https://github.com/taarskog/crm-powerbi-viewer/releases/) \| [Source](https://github.com/taarskog/crm-powerbi-viewer)
{: style="text-align: center"}

<br />
[![]({{BASE_PATH}}/assets/images/v1.0/samples/sample-montage.png)]({{BASE_PATH}}/assets/images/v1.0/samples/sample-montage.png)
<br />

**[Power BI](http://powerbi.com) is the best tool for visualising your business data**. As a customer of Dynamics 365 Customer Engagement you obviously want to take advantage of Power BI inside your dashboards and forms.

Today Dynamics 365 CE support showing Power BI reports and dashboards in your personal dashboards. But the functionality is limited.

**The goal of _crm-powerbi-viewer_ is to deliver as much of the Power BI functionality inside Dynamics 365 as possible.**
{: .alert .alert-information }

Below is a list of enhancements provided by crm-powerbi-viewer that for the time being is _not_ available by using the built-in PowerBI integration in Dynamics 365.

<br />
**Enhancements:**
- Solution aware. _Embed Power BI to any dashboard (not only personal)_
- Embed Power BI to both dashboards and forms
- Works with Dynamics 365 on-premises
- Supports opening reports on a specific page
- Support for custom filters and interactions. Enabling:
    - Open related Dynamics 365 records when clicking on data in a report (or visual)
    - Filter reports on Dynamics 365 data (e.g. filter on account id when showing reports on an account form)
- Hide report navigation and filter panes
- Mix and match multiple Power BI elements with Dynamics 365 elements on a single dashboard/form
- Embed Power BI:
    - Dashboards
    - Single tile from a dashboard
    - Reports
    - Single visual from a report (new in v1.1)

<br />
[![]({{BASE_PATH}}/assets/images/v1.0/samples/sample-montage-dashboards.png)]({{BASE_PATH}}/assets/images/v1.0/samples/sample-montage-dashboards.png)
<br />
<br />
<br />


<br />
[![]({{BASE_PATH}}/assets/images/v1.0/samples/sample-multi-tiles-on-dash.png)]({{BASE_PATH}}/assets/images/v1.0/samples/sample-multi-tiles-on-dash.png)
<br />
<br />
<br />

## Installation

### Prerequisits
You have of course already created a Power BI report or dashboard with tiles you want to embed into your Dynamics 365 instance? 
If not go ahead and do that now. You should create your content in a Workspace for easy sharing with users of Dynamics 365.

As the solution needs to authenticate users against Power BI you need proper rights to add an application
to your Azure Active Directory (AAD). Without such rights you will not be able to make this work.
Reach out to your Azure or Office 365 Admin if you do not have the proper rights.

### Installation steps:

[<span class="badge badge-info">1</span> Add crm-powerbi-viewer as an application in Azure AD](pages/azure-ad.html) (or try the [alternative](pages/azure-ad-simple.html) simpler flow)  
[<span class="badge badge-info">2</span> Install and configure crm-powerbi-viewer in Dynamics 365 Sales and Service](pages/install-solution.html)

Not working as expected? Have a look at [troubleshooting](pages/troubleshooting.html).

<br />

### Basic Configuration

The guide below describe how to add Power BI elements to Dynamics 365 Dashboards.

[<span class="badge badge-info">Dashboard</span> Add a Power BI View to a CRM Dashboard](pages/add-view-to-dashboard.html)   

<br />

**Note** The same steps apply to embedding into CRM Forms.
{: .alert .alert-info }

[![]({{BASE_PATH}}/assets/images/v0.3/samples/sample-crm-montage-3.png)]({{BASE_PATH}}/assets/images/v0.3/samples/sample-crm-montage-3.png)
<br />

### Advanced Configuration - filtering, click-handling, ...

Filtering and handling click-events require some javascripting - how much depend on what you want to achieve. The guide below provides a brief
introduction and links to more information when you want to take it to the next step.

[<span class="badge badge-info">Adv</span> Advanced Configuration](pages/advanced-config.html)   
