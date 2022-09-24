# SynthDash
## A custom theme for [discord-easy-dashboard](https://github.com/SimonLeclere/discord-easy-dashboard)

### Installing

```js
npm i discord-easy-dashboard synthdash
```

### Usage

To get started using the [discord-easy-dashboard](https://github.com/SimonLeclere/discord-easy-dashboard) package read the docs by clicking [here](https://github.com/SimonLeclere/discord-easy-dashboard/blob/master/docs/gettingStarted.md)

To get started using this custom theme in this package use the following code or learn more at the [theming guide](https://github.com/SimonLeclere/discord-easy-dashboard/blob/master/docs/THEMING.md) on the discord-easy-dashboard docs.

```js
const { Client, Intents } = require('discord.js');
const Dashboard = require('discord-easy-dashboard');
const SynthDash = require('synthdash')

const client = new Client({ intents: [Intents.FLAGS.GUILDS, Intents.FLAGS.GUILD_MESSAGES] });

client.dashboard = new Dashboard(client, {
    name: 'Cool Bot',
    description: 'A cool bot with a custom dashboard',
    baseUrl: 'http://localhost',
    port: 80,
    noPortIncallbackUrl: false,
    secret: 'YoUr-Secret_Here',
    theme: SynthDash
});

client.login('Your.Token.Here')
```

## Credits

Simon - Creator of [discord-easy-dashboard](https://github.com/SimonLeclere/discord-easy-dashboard) - View his github [here](https://github.com/SimonLeclere)

Frostzzone - Creator of [SynthDash](https://npmjs.com/package/synthdash) - View his github [here](https://github.com/frostzzone)
