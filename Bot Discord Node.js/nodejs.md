# 🤖 Discord Bot en Node.js avec discord.js (2025)

Ce dossier contient un bot Discord basique en Node.js utilisant la librairie `discord.js`, compatible avec l'API Discord en 2025.

## 📦 Prérequis

- Node.js v20 ou supérieur
- Un bot créé via [Discord Developer Portal](https://discord.com/developers/applications)

## 🚀 Installation

1. Clone le projet et accède au dossier `nodejs-bot` :

```bash
cd nodejs-bot
npm install
```

2. Crée un fichier `.env` contenant ton token :

```env
DISCORD_TOKEN=ton_token_ici
```

## 🧑‍\u💻 Exemple de code

```js
require('dotenv').config();
const { Client, GatewayIntentBits } = require('discord.js');

const client = new Client({
  intents: [GatewayIntentBits.Guilds, GatewayIntentBits.GuildMessages, GatewayIntentBits.MessageContent]
});

client.once('ready', () => {
  console.log(`Connecté en tant que ${client.user.tag}`);
});

client.on('messageCreate', message => {
  if (message.content === '!ping') {
    message.channel.send('Pong!');
  }
});

client.login(process.env.DISCORD_TOKEN);
```

## ▶️ Lancer le bot

```bash
node index.js
```

## 📚 Ressources utiles

- [Documentation discord.js](https://discord.js.org/#/)
- [Discord Developer Portal](https://discord.com/developers/applications)

## 🛡 Licence

MIT License

## 👨‍💻 Auteur

- [konquest.xyz](https://konquest.xyz)