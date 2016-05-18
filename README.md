Office 365 Graph API is a great way to start building applications for Office 365. This sample project will connect the dots from Azure Active Directory to Office 365 Graph APIs. The sample uses HTML & Javascript with Office 365 Graph API.
------------------------------------------------------------------------

----------


***

*To Start the setup please proceed to the following steps and ignore the ones which you already did:*
------------------------------------------------------------------------

------------------------------------------------------------------------

**Step-1:** Signup for Azure trial account, here I am using following credentials:

		ID: xxx.xxx@outlook.com
		Password: xxx@yyyy


**Step-2:** Now signup a new outlook account which will be required for new trial Office 365 developer account and once you signup, proceed to next step.
		ID: xxx.zzz@outlook.com
		Password: zzz@1234


**Step-3:** Signup for Office 365 developer trial account through 
			`https://profile.microsoft.com/RegSysProfileCenter/wizardnp.aspx?wizid=14b845d0-938c-45af-b061-f798fbb4d170&lcid=1033`
	Then check your outlook email account created on Step-2 and signup through the link mentioned in email, following is the highlight:
![Screenshot from email](https://lz20fa-sn3301.files.1drv.com/y3mSr3WVVqGDTMpJtewPJlOeOb1fcwtcVxftDybkwPW15e9b5f2OmLeutDBo-Nh7fNF_cqjyt_aPesNsBQ5TU8K3FC1J9w3qAR2hlwg2P6qILVov0OvmRumVvmqYIUaTATjnUr2lxaD5yolBc8sPoT37JjwVLBnultdEJoNlcxkDIk?width=567&height=155&cropmode=none "Screenshot from email")
> Now you will get the credentials which looks like the following:
	  	**ID:** xxx@yourcompany.onmicrosoft.com
		**Password:** xxxxxxxx


**Step-4:** Associate your existing Azure Subscription with O365 Developer account (refer https://graph.microsoft.io/en-us/docs/authorization/associate_account)

> **Step-4(a):** Login with the Azure Credentials mentioned in Step-1.

> **Step-4(b):** Navigate to Azure Active Directory then create new Active Directory and specify existing directory then sign-out &
> sign-in with the credentials mentioned in Step-3. 


> **Step-4(c):** After that sign-in with the Azure Credentials mentioned in Step-1.


**Step-5:** Now goto Directory with name as < yourcompany > and add the application refer https://azure.microsoft.com/en-us/documentation/articles/active-directory-integrating-applications/

> **Step-5(a):** In AppID URI specify http://localhost:34224/Hello & in Reply URL specify http://localhost:34224/Hello/calendarsample.html
> (assuming this deployment in your local machine)

> **Step-5(b):** Once it is created, click on the application --> Configure then scroll down to permissions to other application and
> Click on Add application

> **Step-5(c):** Click on + in front of Office 365 Exchange Online then click on tick mark.

> **Step-5(d):** Now click on Delegate permissions in front of Office 365 Exchange Online and select the following:
>  1. Read & Write User Calendars 
>  2. Read user Calendars 
>  3. Send mail as a User
> **Step-5(e):** Click on Save then scroll up till client id then copy the client id to sample application.
> 


**Step-6:** Run the calendarsample.html under http://localhost:34224/Hello/calendarsample.html which is specified under Reply to URL while registering application in step-5(a).

> **Step-6(a):** Click on Get Token to authorize specify the following credentials in login page
> > **ID:** xxx@yourcompany.onmicrosoft.com 		
> > **Password:** xxxxxxxx
> 
> This will fill up the token in OAuth Token textbox.

> **Step-6(b):** Now specify details for event then click on Create Calendar. This should open up processing popup then
> confirmation popup.


Please feel free to raise issue in case you came across any, I will try my level best to incorporate soon.

