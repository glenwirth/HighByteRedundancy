This example shows how a primary and secondary base configuration can be setup as deployment packages.  The only difference between the 2 deployments are the Redundancy system settings for the secondary hub.  This version 4.5 deployment can used by anyone since this is a public repository.

To deploly, follow these steps.

1) Install version 4.5
2) Download deployment-settings_PrimaryHub.json, deployment-settings_SecondaryHub and intelligencehub-certificatestore.pkcs12 and place them into your appData folder.
3) Set the HIGHBYTE_DEPLOYMENT_FILE environment variable to the path and deployment settings that you want to deploy.  E.g. C:\Installs\HighByte\appData\deployment-settings_PrimaryHub.json
4) Start Intelligence Hub. The deployment will happen before the hub starts.

Note: 

deployment-settings_PrimaryHub.json - This is a deployment setting file for the primary hub.

deployment-settings_SecondaryHub - This is a deployment setting file for the secondary hub.  It deploys the priamry fragement and also set the Redundancy system settings using a 2nd fragment.   It uses keypath of ".system.settings.redundancy.backup" to just set the Redundancy system settings.

intelligencehub-certificatestore.pkcs12 - This is the default PKCS12 file.   Its password has not been specified.

Once setup, the HighByte Administrator password is: password
