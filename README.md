# skael-pilot API

This project will poll through the configured Gmail address and retrieves all the latest Json messages in the body of an email. Convert the message to Json Object and invoke the REST endpoint 
https://staging.skael.com/api/mulemail

Steps to test this app

1. Send an email to skaelpilot@gmail.com with a content.
2. The above step will trigger this skael-pilot project. This project convert the message to a Json object and invokes the rest endpoint.
3. The REST endpoint logs should contain this Json object.

Steps to deploy this app in Linux environment

1. Install the Mule Standalone application in Linux environment by following the below link https://docs.mulesoft.com/mule-user-guide/v/3.7/downloading-and-starting-mule-esb
   by selecting the tab "Mule EE Runtime + MMC"
2. Copy the deployment archive skael-pilot.zip and paste in standalone apps folder using the below command.
   sudo cp "CopiedZipFileLocation" /"MuleStandaloneHome"/apps (example /opt/mule/mule-standalone-3.8.0/apps)
3. This should dynamically deploy the application in Mule Standalone server.
4. After 2-3 minutes. Test the code by triggering an email to skaelpilot@gmail.com

Commands to start and stop the Mule standalone server in linux box

cd /"MuleStandaloneHOme"/bin (example /opt/mule/mule-standalone-3.8.0/bin)
sudo ./mule stop
sudo ./mule start

Right now this app this directly deployed in Cloudhub to test it directly and below are the cloudhub and gmail credentials.

Cloudhub Account username/password: careersakhilesh/Skael123
Gmail Account username/password: skaelpilot@gmail.com/skael123

