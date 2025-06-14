<a href="https://github.com/mxssl/tg-captcha-bot/graphs/contributors"><img alt="GitHub contributors" src="https://img.shields.io/github/contributors/mxssl/tg-captcha-bot"></a>
<a href="https://github.com/mxssl/tg-captcha-bot/releases/latest"><img alt="GitHub All Releases" src="https://img.shields.io/github/downloads/mxssl/tg-captcha-bot/total"></a>
<a href="https://hub.docker.com/r/mxssl/tg-captcha-bot"><img alt="Docker Pulls" src="https://img.shields.io/docker/pulls/mxssl/tg-captcha-bot"></a>

# Telegram Captcha Bot

Telegram bot that validates new users that enter supergroup. Validation works like a simple captcha. Bot written in Go (Golang).

This bot has been tested on several supergroups (2000+ people) for a long time and has shown its effectiveness against spammers.

## Cloud hosted instance of the bot

[@cloud_tg_captcha_bot](https://t.me/cloud_tg_captcha_bot)

## How it works

1. Add the bot to your supergroup
2. Promote the bot for administrator privileges
3. A new user enters your supergroup
4. Bot restricts the user's ability to send messages
5. Bot shows a welcome message and a captcha button to the user
6. If the user doesn't press the button within 30 seconds then the user is banned by the bot

## If you want to run your own instance of the bot

- [Option 1 (the easiest one)](./INSTALL-1.md): docker-compose + already built docker container
- [Option 2](./INSTALL-2.md): docker-compose + build your own docker container
- [Option 3](./INSTALL-3.md): systemd

## Commands

`/healthz` - check that the bot is working correctly

## Сustomization

You can change several bot's settings (welcome message, ban duration, socks5 proxy server) through the configuration file `config.toml`

## Alternatives / Forks

- [momai/tg-captcha-bot](https://github.com/momai/tg-captcha-bot) - fork of `tg-captcha-bot` with interesting additional features.
