# mule4tips
Some tips to help in Mule4

# DataWeave 2: get current server time
https://github.com/thiago-devel/mule4tips/blob/master/millis.DW

# DataWeave 2: build date time in Json format
https://github.com/thiago-devel/mule4tips/blob/master/datetime.DW

# Mule 4: logging migration process from Mule 3.x to Mule4 example project
https://github.com/thiago-devel/mule4tips/tree/master/loggingMule4

# Design Center x Studio7 X API Manager: ERROR 503 running local host app
If you are implementing a Managed API imported from Design Center on your Studio 7 and after to add the autodiscovery ID componet, the application starts to always return a strange error 503 - with nothing being shown at the console - confirm if your Anypoint Platform organization client_id and client_secret are correctly configurated at your Studio.
Path: Preferences>Anypoint Studio>API Manager
Fill the client_id and client_secret fields and click in validate.

Obs: If even after a succesfully deploy of your application to the Runtime Manager your API Manager keep locked/inactive. Go to Runtime Manager>your app settings>Properties and add the below (without quotes):

anypoint.platform.analytics_base_uri="https://analytics-ingest.anypoint.mulesoft.com/"
anypoint.platform.client_id= "your organization client id"
anypoint.platform.client_secret= "your organization client secret"
anypoint.platform.base_uri="https://anypoint.mulesoft.com/"
