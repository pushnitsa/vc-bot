# Virto Commerce Order Bot. Configuration instructions

## Prerequisites
* Azure subscription https://azure.microsoft.com/en-us/free/
* Access to running Virto Commerce Platform

## Configuring platform and bot
1. Create "BotUserName" dynamic property (Value Type: Short Text) to VirtoCommerce.Domain.Customer.Model.Contact type. Restart the application.
2. Create security account for authenticating as a bot. 
   * Mark it "Is administrator".
   * Add API Account (Hmac type)
3. Fill VirtoCommerce.OrderBot\appsettings.json

## Deploy to Azure
1. Sign in to Azure portal
2. Create Bot Channel (Create a resource -> Bot Channels Registration)
3. Add application secrets (Registered bot channels -> Settings -> Microsoft App ID (Manage))
4. Fill "AppId" and "SecretKey" in the VirtoCommerce.OrderBot\appsettings.json
5. Deploy bot as regular web application
6. Fill Messaging endpoint (Registered bot channels -> Settings -> Messaging endpoint) (applicationEndpoint/api/messages)
7. Add channels as you need
8. Enjoy!

https://docs.microsoft.com/en-us/azure/bot-service/bot-builder-deploy-az-cli?view=azure-bot-service-4.0

## Bot authorization

The first time when you contact the bot, it will send you your identifier. You need to save the identifier to your Contact's dynamic property (BotUserName), reindex the entity, and try to authorize with the bot.