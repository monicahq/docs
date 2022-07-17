---
id: introduction
title: Installation
sidebar_label: Installation
sidebar_position: 1
---

### Setup Telegram for development

Users can setup Telegram to receive notifications. This is a bit tricky to set up from an instance's administration point of view if you want to test locally.

First of all, you need to setup a Telegram bot to be able to receive notifications. Then you need to configure Monica with the right env variables. Finally, you need to send the webhook URL to Telegram so Telegram can communicate with your local setup.

1. Follow the first steps described in https://docs.microsoft.com/en-us/azure/bot-service/bot-service-channel-connect-telegram?view=azure-bot-service-4.0 so you create a bot. Note that you will need the token that Telegram will send you right after creating your bot.

2. Fill the three env variables about Telegram. These below are obviously fake values.

```
TELEGRAM_BOT_TOKEN=393828013:AAEaw8whKIdkW2EIy23ksVY51XQqsV7o_3M
TELEGRAM_BOT_URL=https://t.me/YOUR_BOT_NAME
TELEGRAM_BOT_WEBHOOK_URL=lkjl2kjl2k323oIOWEJFkek (RANDOM STRINGS OF MANY CHARACTERS (25+))
```

3. Tell Telegram which URL it should use to send you notifications. In production, that would be the URL of your server, but for development, it's your URL fronted by NGrok or Expose which will create a tunnel between your local environment and Telegram.

That means, assuming you've run [Expose](https://expose.dev/), the webhook URL would be:

`https://EXPOSE OR NGROK URL.'/telegram/webhook/'.YOUR TELEGRAM BOT WEBHOOK URL`

or with real fake values:

https://eklpjfbrpq.sharedwithexpose.com/telegram/webhook/lkjl2kjl2k323oIOWEJFkek/

Then, to inform Telegram, copy and paste the following in your browser.

`https://api.telegram.org/bot[393828013:AAEae8whNPAHi2EIyRmssVY51XQqsV7o_3M]/setWebhook?url=[https://EXPOSE OR NGROK URL.'/telegram/webhook/'.YOUR TELEGRAM BOT WEBHOOK URL]`

or with real (fake) values:

https://api.telegram.org/bot393828013:AAEaeEFKEJNPAHi2EIyRmssVY51XQqsV7o_3M/setWebhook?url=https://eklpjfbrpq.sharedwithexpose.com/telegram/webhook/lkjl2kjl2k323oIOWEJFkek/

Telegram should send you the following as the return of this query:

```json
{"ok":true,"result":true,"description":"Webhook was set"}
```

This means your Telegram setup is completed.