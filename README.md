# MDSecPwrBi
**About**
This is a PowerBi Template designed to profile connection traffic. This can be used as an overview for aiding in building firewall profiles, troubleshooting and trend identification. 

**Requirements to Use**
The template harvests data from https://api.securitycenter.windows.com/api/. This harvest requires a subscription to Microsoft's Defender for the Endpoint (MDE). The MDE portal can be found here: https://security.microsoft.com. From the MDE portal the account that opens the Power Bi template will need the ability to run a hunting query. 

Power BI Desktop will need to be installed. Power Bi Desktop is Free. It is ideal to install the 64 bit version. The Windows store version of Power Bi is the 32 bit version. There are legacy conditional access settings that will require the machine used to open this template be either hybrid Azure AD joined or Azure AD joined to use the API for Security Center.

If the dashboard were going to be published to a publicly accessible dashboard it would require a Power Bi Cal (licenses). The benefit to publishing the dashboard is that it would be accessible to individuals without the Power BI Desktop software installed and that permissions to the dashboard could be set on the dashboard. 

There is also a seperate API call to http://api.ipstack.com. The API call to IPStack is for geolocation IP data.  Replace the key in the advanced editor (in the Power Bi Template) with your own key if you opt to leverage the two pages within the template that show IP location. There is a free version available for this tool. You can leverage a seperate geolocation database but it will require modification of data gathering utility.


**Troubleshooting**

-Connectors

You may need to enable connectors for the geolocation api to work
https://learn.microsoft.com/en-us/power-bi/connect-data/desktop-connector-extensibility

-Maps

In order for the maps visuals to work the setting will need to be enabled. 
https://learn.microsoft.com/en-us/azure/azure-maps/power-bi-visual-get-started#azure-maps-power-bi-visual-behavior-and-requirements 

-Clear Cache

https://support.biconnector.com/support/solutions/articles/8000072804-how-to-clear-cache-of-power-bi-desktop-

-API Connection 

Basics:
https://learn.microsoft.com/en-us/microsoft-365/security/defender-endpoint/api-power-bi?view=o365-worldwide

There is also a set of legacy conditional access settings in the Microsoft Endpoint Management Portal that requires your machine be Hybrid or Azure AD Joined to leverage the api directly. If you cannot connect due to these constraints with Power BI desktop because of this you can remove the classic policy. It is reccommended that you add back a modern policy doing something very similar.  

https://techcommunity.microsoft.com/t5/microsoft-defender-for-endpoint/classic-conditional-access-policy-for-defender-atp/m-p/1883297


**Disclaimer**
This is provided as is and comes with no warranty or gaurantee. 
