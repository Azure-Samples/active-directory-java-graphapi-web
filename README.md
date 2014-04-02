WebApp-GraphAPI-Java
====================
This Java sample application is a web app that reads directory data from the Windows Azure Active Directory Graph API, and executes queries against a demo company. The full list of capabilities for the Graph API can be found on MSDN (link below). If you would like to access your own Azure AD tenant's directory data, then the application must be configured with your own Tenant ID, Application ID and App Key - these values are stored in the app's web.xml file, then rebuild the application. 


## How To Run This Sample

Getting started is simple!  To run this sample you will need:
- JDK 7 Standard Edition (JDK7 or greater)
- Eclipse IDE
- Apache Tomcat
- An Internet connection
- An Azure subscription (a free trial is sufficient)

Every Azure subscription has an associated Azure Active Directory tenant.  If you don't already have an Azure subscription, you can get a free subscription by signing up at [http://wwww.windowsazure.com](http://www.windowsazure.com).  All of the Azure AD features used by this sample are available free of charge.

### Step 1:  Clone or download this repository

From your shell or command line:

`git clone git@github.com:AzureADSamples/WebApp-GraphAPI-Java.git`

### Step 2:  Create a user account in your Azure Active Directory tenant

If you already have a user account in your Azure Active Directory tenant, you can skip to the next step.  This sample will not work with a Microsoft account, so if you signed in to the Azure portal with a Microsoft account and have never created a user account in your directory before, you need to do that now.  If you create an account and want to use it to sign-in to the Azure portal, don't forget to add the user account as a co-administrator of your Azure subscription.

### Step 3:  Register the sample with your Azure Active Directory tenant

 1. Sign in to the [Azure management portal](https://manage.windowsazure.com).
 2. Click on Active Directory in the left hand nav.
 3. Click the directory tenant where you wish to register the sample application.
 4. Click the Applications tab.
 5. In the drawer, click Add.
 6. Click "Add an application my organization is developing".
 7. Enter a friendly name for the application, for example "WebApp-GraphAPI-Java", select "Web Application and/or Web API", and click next.
 8. For the sign-on URL, enter the base URL for the sample, which is by default `https://localhost:44320`.
 9. For the App ID URI, enter `https://<your_tenant_name>/WebApp`, replacing `<your_tenant_name>` with the name of your Azure AD tenant.

All done!  Before moving on to the next step, you need to find the Client ID of your application, and create an App Key.

 1. While still in the Azure portal, click the Configure tab of your application.
 2. Find the Client ID value and copy it to the clipboard.
 3. Add a key - select a key duration of either 1 year or 2 year. When you save this page, the key value will be displayed, copy and save the value in a safe location - you will need this key later to configurate the Client Credentials for this app - this key value will not be displayed again, nor retrievable by any other means, so please record it as soon as it is visible from the Azure Portal.

### Step 4:  Configure the sample to use your Azure Active Directory tenant

The Sample application can be built using the Eclipse IDE, and runs under Tomcat.The following instructions are provided:

 1.Download and install the JDK 7 from the Oracle Website (select the version for your development environment (e.g. Windows x64) JDK 7 
 2. Select JDK Standard Edition (JDK SE 7 with latest update).
 3. Set a system environmental variable named JAVA_HOME and give the variable value to your java installation. Typically, this value would be something like: C:\Program Files\Java\jdk1.7.0_06
 4.Download and install the Eclipse IDE for Java EE Developers from the following website (select the version for your development environment (e.g. Windows x86).  Eclipse IDE for Java EE   
   To start Eclipse, simply execute Eclipse.exe
 5. Download and install Apache Tomcat.   Apache TomCat  (http://tomcat.apache.org/)
     You can run Apache Tomcat by clicking <tomcat folder>/bin/startup.bat script. You can also shut down apache tomcat by clicking <tomcat folder>/bin/shutdown.bat. When running your application from Eclipse, it can be configured to automatically start Apache Tomcat, and execute in normal or debug mode. 

 6.Import the project in Eclipse by:
  a. Starting Eclipse by clicking Eclipse.exe.
  b. Specify a workspace folder of your choice.
  c. Click File/Import/General/Existing Projects Into the workspace
  d. Select the root directory to the project you want to import into.
  e. Click Finish.  

Optionally, you can also import the JavaSampleApp.war file by selecting from Eclispe:  File/Import/Web/War and selecting the JavaSampleApp.war file.

 7. To see the opened project:
  a. Click Window/Show View/Project Explorer. This would show the project explorer which would show the whole project hierarchy on
     the left of your screen.
  b. Now right click on the project name, and select ‘Run As/Run on Server’.
  c. This would prompt you to specify a server                                                           
     i. Select Apache Tomcat V7.0                                                             
     ii. Select the root directory of the tomcat server.                                                          
     iii. Select “Always use this server”.

## About The Code

Coming Soon.