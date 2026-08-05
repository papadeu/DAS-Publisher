# DAS-Publisher

This application monitors given DAS Trader account in real time and sends a message to main app window and/or to given text channel (via web-hook) when trade execution occured. All web-hook channels are supported, i.e. Discord, Slack etc.

A local instance of DAS Trader must run on the same machine where this application is used.

It doesn't influence DAS Trader performance in any way, due to usage of "DAS CMD API".

This application uses DAS API in 'read only' mode however user credentials are required to monitor account's positions.
User password is stored locally in encrypted way. DAS API 'read only' is free of charge and included in basic DAS version..

All communication between Publisher and DAS occurs locally.

Publisher does not execute any transations on connected account ('read only').

The entire C# .NET8 source code is published here for transparency purpose. You can compile the source code by yourself using MS VisualStudio or you can use already compiled executable file which is inside Executable.zip. There are 2 files: an exe and a config file to store the publishing settings inside it. 

Prerequisities for using:

   1)  .NET8 Framework installed on local machine, please take ".NET Desktop Runtime" option: download from here: https://dotnet.microsoft.com/en-us/download/dotnet/8.0

Optionally:
   1)  Existing text channel web-hook:
     A)  example Slack: https://docs.slack.dev/messaging/sending-messages-using-incoming-webhooks/

For deploying as user (not developer) please download the existing 2 files (Executable.zip) to your local windows folder and start the executable:
DasPublisher.exe and DasPublisher.dll.config (which is a text file)

Published source code is only for transparency purpose, to show that no other actions except read only account's position monitoring and http send request to given WebHook URL are made with this software. 


DAS Trader must be configured for using API:

   1)  In DAS go to “Setup/OtherConfiguration/Configuration/CMDAPI Settings”, set the CMDAPI port number (i.e. 7001) and take it into corresponding DasPublisher's field.


<img width="1525" height="576" alt="grafik" src="https://github.com/user-attachments/assets/be5c0c32-023b-45e3-90b8-49a5ea49ebd9" />

<img width="743" height="423" alt="grafik" src="https://github.com/user-attachments/assets/a14fd571-599a-4f32-bb00-268b97391734" />

<img width="666" height="252" alt="grafik" src="https://github.com/user-attachments/assets/69dc6132-0d22-4280-823e-e83f34d8bba2" />


