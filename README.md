# Kindly Starter Kit for Javascript

Build your first chatbot integration using the Kindly&trade; platform.

## Quick start :rocket:

The fastest way to get started is to deploy this repo using Heroku.

Hit the button below to start the deployment. If you don't already have an account on Heroku, you'll have to create one. Don't worry, its free to try out.

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/convertelligence/kindly-starterkit-js/tree/master)

You'll be asked to give the Heroku application a name, select a region (US or Europe) and enter a `KINDLY_API_KEY`.

To create an API key, go to the [Kindly platform](https://platform.convertelligence.com). Navigate to your bot. Go to Connect from the sidebar menu. If you haven't already created an Application, do it now. Now go to the Application you created. Press "Show API key" and copy-paste the API into the `KINDLY_API_KEY` field.

Once the deployment is done, click View app. Copy the URL from the web page and paste it into a dialogue webhook url. Now open the chatbubble and try to make your chatbot trigger the dialogue.

:tada: Congratulations! You've integrated your first chatbot! :sparkles:

## Getting started with local development

Now for the fun part: Come up with an integration idea! [Check out this list](https://github.com/abhishekbanthia/Public-APIs) for tips! :runner:

:bulb: Once you've found the perfect idea for a bot integration, you should clone this repo by opening your terminal and running the following commands:

```
git clone https://github.com/convertelligence/kindly-starterkit-js.git
cd kindly-starterkit-js
cp .env.default .env
```

To add your newly created Heroku application as a remote, which will allow you to push updates to the application, run the following command:

`heroku git:remote -a your_heroku_app`

Replace `your_heroku_app` with your Heroku application name.

### Set up your Kindly API key

Before you continue, open up the `.env` file in your editor.

Set the `KINDLY_API_KEY` value to the API key from your Kindly Application.

Now that that's taken care of, you're ready to continue the setup process:

```
npm install
source .env
npm start
```

:tada: If everything went smoothly, you should have a webserver running at [http://localhost:9292](http://localhost:9292) that you can use for further development.

If you accidentally close your webserver at any point and want to restart it, you can do so by running

`npm start` :+1:

### Using ngrok to develop locally

Start `ngrok` so you can tunnel requests from Kindly to your local app:

`ngrok http 9292`

This way you dont need to deploy the app to Heroku every time you make a change. You now have a ngrok URL that you can use to plug in to Kindly dialogues.
