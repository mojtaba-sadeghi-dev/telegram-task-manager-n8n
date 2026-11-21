
# Telegram Task Manager with n8n

A Telegram-based task management automation built with
n8n and Google Sheets.

## Overview

This project allows users to manage tasks directly
through a Telegram bot.

The workflow receives Telegram messages, processes
task commands, stores data in Google Sheets, and
sends confirmation messages back to Telegram.

## Tech Stack

- n8n
- Telegram Bot API
- Google Sheets API
- JavaScript
- Google OAuth2

## Features

- Add new tasks using Telegram messages
- Store tasks in Google Sheets
- List pending tasks
- Mark tasks as completed
- Save creation and completion timestamps
- Support basic Persian commands and date parsing

## Tested Commands

/add Learn Python
/list
/done TASK_ID

The /start command also provides usage instructions.

The /today feature is implemented but has not yet
been independently verified.

## Setup

1. Import `workflow.json` into n8n.
2. Create a Google Sheet named `Tasks`.
3. Add the required columns using the provided CSV.
4. Configure Telegram credentials.
5. Configure Google Sheets OAuth2 credentials.
6. Set the Google Spreadsheet ID in all four
   Google Sheets nodes.
7. Configure a public HTTPS webhook URL for
   Telegram Trigger.
8. Test the workflow and activate it.

## Security

- No API keys or access tokens are included.
- Configure credentials in your own n8n instance.
- Do not publish private spreadsheet data.
- Restrict Telegram access if using the bot privately.

## Limitations

- Uses rule-based command processing, not an LLM.
- Natural-language parsing is limited.
- Dates are based on the Asia/Tehran timezone.
- Telegram webhooks require publicly reachable HTTPS.

## Project Status

Core functionality tested:
- Task creation
- Task listing
- Task completion

## Author

Mojtaba Sadeghi

GitHub: https://github.com/mojtaba-sadeghi-dev
