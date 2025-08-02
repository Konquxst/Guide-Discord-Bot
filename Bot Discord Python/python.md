# 🤖 Discord Bot en Python avec discord.py (2025)

Ce dossier contient un bot Discord basique en Python utilisant la librairie `discord.py`, compatible avec l'API Discord en 2025.

## 📦 Prérequis

- Python 3.11 ou supérieur
- `discord.py` installé (version stable)
- Un bot Discord créé sur le [Discord Developer Portal](https://discord.com/developers/applications)

## 🚀 Installation

1. Clone ce dépôt et accède au dossier `python-bot` :

```bash
cd python-bot
python -m venv venv
source venv/bin/activate  # Windows : venv\Scripts\activate
pip install -U discord.py
```

2. Crée un fichier `.env` pour stocker ton token :

```
DISCORD_TOKEN=ton_token_ici
```

Installe `python-dotenv` si tu veux utiliser `.env` :
```bash
pip install python-dotenv
```

## 🧑‍\u💻 Exemple de code

```python
import os
import discord
from discord.ext import commands
from dotenv import load_dotenv

load_dotenv()
TOKEN = os.getenv("DISCORD_TOKEN")

intents = discord.Intents.default()
intents.message_content = True
bot = commands.Bot(command_prefix="!", intents=intents)

@bot.event
async def on_ready():
    print(f"Connecté en tant que {bot.user}")

@bot.command()
async def ping(ctx):
    await ctx.send("Pong!")

bot.run(TOKEN)
```

## ▶️ Lancer le bot

```bash
python bot.py
```

## 📚 Ressources utiles

- [Documentation discord.py](https://discordpy.readthedocs.io/en/stable/)
- [Discord Developer Portal](https://discord.com/developers/applications)

## 🛡 Licence

MIT License

## 👨‍💻 Auteur

- [konquest.xyz](https://konquest.xyz)