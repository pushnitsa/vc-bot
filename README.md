# VirtoCommerce order bot instructions

## Configuring platform and bot
1. Add dynamic property "BotUserName" (ShortText type) to a contact. Restart application.
2. Add bot's security account. Make it an Administrator.
3. Add API Account (Hmac type)
4. Fill VirtoCommerce.OrderBot\appsettings.json

## Deploy to Azure
1. Sign in Azure portal
2. Create Bot Channel (Create a resource -> Bot Channels Registration)
3. Add application secrets (Registered bot channels -> Settings -> Microsoft App ID (Manage))
4. Fill "AppId" and "SecretKey" in the VirtoCommerce.OrderBot\appsettings.json
5. Deploy bot as regular web application
6. Fill Messaging endpoint (Registered bot channels -> Settings -> Messaging endpoint) (applicationEndpoint/api/messages)
7. Add channels as you need
8. Enjoy!

https://docs.microsoft.com/en-us/azure/bot-service/bot-builder-deploy-az-cli?view=azure-bot-service-4.0