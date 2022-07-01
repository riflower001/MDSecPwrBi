# MDSecPwrBi
**About**
This is a PowerBi Template designed to profile connection traffic. This can be used as an overview for aiding in building firewall profiles, troubleshooting and trend identification. 

**Requirements to Use**
The template harvests data from https://api.securitycenter.windows.com/api/. This harvest requires a subscription to Microsoft's Defender for the Endpoint (MDE). The MDE portal can be found here: https://security.microsoft.com. From the MDE portal the account that opens the Power Bi template will need the ability to run a hunting query. 

Power BI Desktop will need to be installed. Power Bi Desktop is Free. It is ideal to install the 64 bit version. The Windows store version of Power Bi is the 32 bit version. 

If the dashboard were going to be published to a publicly accessible dashboard it would require a Power Bi Cal (licenses). The benefit to publishing the dashboard is that it would be accessible to individuals without the Power BI Desktop software installed and that permissions to the dashboard could be set on the dashboard. 
There are legacy conditional access settings that will require the machine used to open this template be either hybrid Azure AD joined or Azure AD joined to connect to the API for Security Center.

There is also a seperate API call to http://api.ipstack.com. The API call to IPStack is for geolocation IP data.  Replace the key in the advanced editor (in the Power Bi Template) with your own key if you opt to leverage the two pages within the template that show IP location. There is a free version available for this tool. You can leverage a seperate geolocation database but it will require modification of data gathering utility.

**Disclaimer**
This is provided as is and comes with no warranty or gaurantee. 
