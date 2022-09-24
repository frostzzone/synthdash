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

## Extra

Use frost's edited version of [discord-easy-dashboard](https://github.com/SimonLeclere/discord-easy-dashboard) by running 

    npm install https://github.com/frostzzone/discord-easy-dashboard
   
or if your using yarn

    yarn add https://github.com/frostzzone/discord-easy-dashboard
    
to add custom footers

Edited dashboard code:
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
    customData:{
        all:{
            footer:{
                text: "hallo"
                color: "#ff0000"
            }
        }
    }
});

client.login('Your.Token.Here')
```

allowed custom data
| top      | layer 1  | layer 2     | what it does                |
| :---:    | :---:    | :---:       | :---:                       |
| all      | footer   | text, color | Set footer on every page    |
| home     | footer   | text, color | Set footer on home page     |
| error    | footer   | text, color | Set footer on error page    |
| commands | footer   | text, color | Set footer on commands page |
| guilds   | footer   | text, color | Set footer on guild page    |
| settings | footer   | text, color | Set footer on settings page |
|          | detail   |             | Change "Edit this guilds settings here" to what ever you want |

footer Example:
![image](https://user-images.githubusercontent.com/65735427/192074063-1a580eb3-7dda-4436-a181-933b70d35555.png)

## Examples
- Home page
![image](https://user-images.githubusercontent.com/65735427/192072766-3aec5585-6c33-4fa9-bb42-c845991c141b.png)

- Guild page
![image](https://user-images.githubusercontent.com/65735427/192073011-f0bf91f1-2940-493d-8185-5fe971cd30ae.png)

- Settings page
![image](https://user-images.githubusercontent.com/65735427/192073221-8b124cba-73b9-4b0f-b2eb-a1d693269ff7.png)
![image](https://user-images.githubusercontent.com/65735427/192073392-b218e564-98ad-4109-81dc-83e32a2694d3.png)

- Commands page
![image](https://user-images.githubusercontent.com/65735427/192073453-43d409ef-b842-4b36-bf52-851455440ec6.png)

## Credits

Simon - Creator of [discord-easy-dashboard](https://github.com/SimonLeclere/discord-easy-dashboard) - View his github [here](https://github.com/SimonLeclere)

Frostzzone - Creator of [SynthDash](https://npmjs.com/package/synthdash) - View his github [here](https://github.com/frostzzone)
