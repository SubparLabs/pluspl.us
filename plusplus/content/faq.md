Here are some commonly asked questions about plusplus's capabilities, operations and other details.


#### What data is collected and what do you do with it?

This app is run for fun and not for profit. Accordingly, while we **can** gaurantee that we'll never sell or otherwise commercialize your data, we don't really have the robust security measures in place that you'd expect from a service that you pay for. When you invite the bot into a channel in your Slack group, _every single message_ in that channel will be sent to our service. Unfortunately there's no filter that can be applied upstream of our service in the Slack API... it is kind of a firehose situation. Our backend looks to see if there's anything relevant to plusplus in each message, does a thing (increment, display leaderboard, etc.) if there is, and then discards the message. You can see the relevant bit of code [here](https://github.com/SubparLabs/pluspl.us/blob/master/plusplus/operations/slack_handler.py). Aside from point totals, we also store your slack _team domain_ and _team ID_. Our privacy policy can be viewed [here](/privacy_policy).

#### Haven't I seen this app before under a different name?

Probably. We first ran into this sort of thing as part of [Hubot](https://github.com/hubot-scripts/hubot-plusplus). Then in the Slack chat bot boom it was packaged as a centralized service under the now defunct [plusplus.chat](http://plusplus.chat). Then a self-hosted, open-source JavaScript version was made [here](https://github.com/tdmalone/working-plusplus). When plusplus.chat went under a python version was resurrected as [pluspl.us](https://go.pluspl.us). When pluspl.us shut down we [forked it](https://github.com/plusplusslack/pluspl.us) and stood it up here at [plusplus.fun](https://plusplus.fun). 

#### What operations are supported right now?

`++`, `--`. and `==` (plus, minus, and equals) are supported for both people and things. Additionally, `@plusplus leaderboard` and `@plusplus loserboard` is also supported to get the local high and low scores. 

#### How do I find the things or users with the most points?

Just type `@plusplus leaderboard` and the top 10 users and things will be displayed.

#### How do I find the things or users with the least points?

Just type `@plusplus loserboard` and the bottom 10 users and things will be displayed.

#### Is there a shortcut to see the instructions within Slack?

Yup! Type `@plusplus help` in your Slack channel or in a private message to the bot and the it will send a list of commands back.

#### Is there a way to delete my team's data from you servers or alter the data?

Send an email to plusplus@subpar.biz and we'll work something out.

#### Is this app open-source?

It is! You can find the source for plusplus on GitHub [here](https://github.com/SubparLabs/pluspl.us). 
