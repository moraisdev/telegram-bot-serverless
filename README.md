# Serverless Telegram Bot

Bot looks for movies and responds to user with all data.

## Usage

### What do I need?
- A AWS key configured locally, see [here](https://serverless.com/framework/docs/providers/aws/guide/credentials/).
- Python 3.8.
- NodeJS.
- A Telegram account.

### Installing
```
# Install the Serverless Framework
$ npm install serverless -g

# Install the necessary plugins
$ npm install

# Create and active a Python 3.8 venv
$ python3.8 -m venv venv && souce venv/bin/activate

# Get a bot from Telegram, sending this message to @BotFather
$ /newbot

# Put the token received into a file called serverless.env.yml, like this
$ cat serverless.env.yml
TELEGRAM_TOKEN: <your_token>

# Deploy it!
$ serverless deploy

# With the URL returned in the output, configure the Webhook
$ curl -X POST https://<your_url>.amazonaws.com/dev/set_webhook
