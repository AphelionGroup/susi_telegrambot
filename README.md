# AskSusi Messengers

[![Code Climate](https://codeclimate.com/github/fossasia/asksusi_messengers/badges/gpa.svg)](https://codeclimate.com/github/fossasia/asksusi_messengers)
[![Build Status](https://travis-ci.org/fossasia/asksusi_messengers.svg?branch=development)](https://travis-ci.org/fossasia/asksusi_messengers)
[![CircleCI](https://img.shields.io/circleci/project/fossasia/asksusi_messengers.svg?maxAge=2592000?style=flat-square)](https://circleci.com/gh/fossasia/asksusi_messengers)
<a href="https://slack.com/oauth/authorize?scope=incoming-webhook,bot&client_id=62652302743.69257872898"><img alt="Add to Slack" height="40" width="139" src="https://platform.slack-edge.com/img/add_to_slack.png" srcset="https://platform.slack-edge.com/img/add_to_slack.png 1x, https://platform.slack-edge.com/img/add_to_slack@2x.png 2x" /></a>

AskSusi is a messengers service that answers your question by using big data from loklak and a number of API services. In this we keep AskSusi chatbots for social media platforms. We have integrated AskSusi on Facebook Messenger, Slack and Telegram. All of these bots / messengers work from one central ```index.js``` file, and run from one URL (with different paths). The type of questions Susi can currently answer can be found in the loklak documentation [here](https://github.com/loklak/loklak_server/blob/development/docs/AskSUSI.md). 

### Messenger Bot for Susi

A live version of Susi's Messenger bot can be found on [facebook.com/asksusisu/](https://www.facebook.com/asksusisu/). Personal Message the page to speak to Susi.

![Susi Messenger](docs/images/messenger_screenshot.png "Susi Messenger")

### How do I install AskSusi on Facebook

For making your own Messenger Bot for Susi, you can check out the Installation doc [here](/docs/INSTALLATION_FACEBOOK.md).

### Slack Bot for Susi

You can directly talk to Susi using the ```Add to Susi``` button above. Click on that button, and add Susi to your team. Talk to it by typing ```@susi``` followed by your message.

![Susi Slack](docs/images/slack_screenshot.png "Susi Slack")

### How do I install AskSuSi on Slack

For making your own Slack Bot for Susi, you can check out the Installation doc [here](/docs/INSTALLATION_SLACK.md).

### Telegram Bot for Susi

A live version of Susi's Telegram Bot can be found [here](https://web.telegram.org/#/im?p=@asksusi_bot). 

![Susi Telegram](docs/images/telegram_screenshot.png "Susi Telegram")

### How do I install AskSusi on Telegram

For making your own Telegram Bot for Susi, you can check out the Installation doc [here](/docs/INSTALLATION_TELEGRAM.md).

## Roadmap

We want to see AskSusi on more platform. Please help us to develop AskSusi bots for other platforms. 

## Technology Stack

As of now, all the bots have been developed in ```node.js``` and ```Express``` for smooth builds and CI, so if you wish to add more bots, you'll have to make your bot in that platform. For contributing, please follow the following instructions:

* Please append your code in the ```index.js``` file (without altering the other bots). Add a comment line specifying your platform, like:
```// <platform> BOT FOR SUSI```
and then write your code below it.

* Update the ```package.json``` with your external ```npm``` packages (if you are using them), i.e when you wish to use an external dependancy for your bot, just add the ```save``` flag as well:

	```npm install --save <package>```

* Add the installation / deployment instructions for your bot in the ```installation_docs``` folder, in a ```.md``` file. Keep the filename as ```<botplatform>.md```. You should write how to setup such a bot on your platform, and how to make it consume the Susi API. To get a better idea, you can check the instructions of the other docs [here](/installation_docs).

* Add a screenshot of your working bot, along with usage (i.e message format) in the ```README.md```. Also write that the installation instructions of your bot can be found at ```<link to your installation documentation>```.

* Finally, send a **single**, **squashed** PR containing all these changes. Please send your PRs to the ```development``` branch as mentioned earlier.

## Branch Policy

The default branch is ```development```, so make sure you contribute only on this branch.

## License

This project is licensed under the GNU GENERAL PUBLIC LICENSE, Version 3. Please find more info in our [license document](LICENSE.md).
