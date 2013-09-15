doothings-bot
==========

bot for #doothings on freenode

# Instructions for deploying on Heroku

Clone the repo.
Change the name `doobot` to name of your bot.
Below is an example of deploying `doobot` on heroku.

``` shell
heroku create punerbot --stack cedar
git push heroku master
heroku config:add HUBOT_IRC_SERVER="irc.freenode.net"
heroku config:add HUBOT_IRC_ROOMS="#doothings"
heroku config:add HUBOT_IRC_NICK="doobot"
heroku config:add HUBOT_IRC_DEBUG="true"
heroku ps:scale app=1
```
