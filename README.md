# «Telegram Callback» Joomla module

![Version](https://img.shields.io/badge/VERSION-1.2.0-0366d6.svg?style=for-the-badge)
![Joomla](https://img.shields.io/badge/joomla-3.7+-1A3867.svg?style=for-the-badge)
![Php](https://img.shields.io/badge/php-5.6+-8892BF.svg?style=for-the-badge)

**ATTENTION! current version is not compatible with version 1.0.0!**

_description in Russian [here](README.ru.md)_

A feedback module sending the message in the telegram, the modern service of instant messages.

A message from the form module goes into pre-created bot.

The bot is created with another system of the bot.

## Description

The default field list is empty, because the need to fill it, then save. Supported field types: text, email, url, tel, password, textarea, select, checkbox, radio. Each field must have a name (for form creation) and name (the identification field in the message in the telegram).

You can also specify a title for the message telegram, if the header is not specified, the default string of the form "Message from website {url}".

The module supports overriding the templates of the messages sent to telegram. Templates are located in the /layouts folder.

The module does not contain embedded CSS and JS, but the layout of the form template is presented in three versions: bootstrap2 (default), bootstrap3/4, uikit2, uikit3.

The message about the successful sending of the post or error is displayed through the standard Joomla system messages.

**ATTENTION!** Must be off `open_basedir` because it does not work used in the module curl.

---

## How to create a bot

- we find in the telegram bot named @BotFather (or follow the link http://t.me/botfather);
- enter the bot the command `/newbot` (or select it from the list of commands in a welcome message);
- consistently enter first name of the bot (any one will come up), then the system nickname, consisting of only Latin characters, digits and "_"symbol;
- voila! we say that the bot created and offer a quick link to it as well &ndash; caution! &ndash; a security token, a kind of universal key to the created bot;
- open the newly created telegram bot and enter the command `/start`, thereby running the bot (this is important!).

In the options installed on site module "Telegram callback" input received when creating a bot token, then click the button "Get ID" chat &ndash; the appropriate box should be filled. If newly created bot was not running the command `/start`, nothing happens. ID chat cannot be obtained if the bot received reports from other sources, in addition to chat in telegram.
