# discord-py-slash-command
Simple Discord Slash Command extension for [discord.py](https://github.com/Rapptz/discord.py).

## Example
```py
import discord
from discord.ext import commands
from discord_slash import SlashCommand
from discord_slash.model import SlashContext

bot = commands.Bot(command_prefix="!", intents=discord.Intents.all())
slash = SlashCommand(bot)


@slash.slash(name="test")
async def _test(ctx: SlashContext):
    embed = discord.Embed(title="embed test")
    await ctx.send(content="test", embeds=[embed])


bot.run("discord_token")
```

## Installation
`pip install -U discord-py-slash-command`

## Simple note before you use this
Since slash command feature is not officially released, 
there will be many breaking changes to this extension and may be unstable, 
so I'd recommend waiting until discord officially releases slash command, 
and wait until Release 1.1.0, which I'm planning to finish implementing most of the feature.  
Or you can wait until discord.py supports slash command.

## DOCS
https://discord-py-slash-command.readthedocs.io/en/latest/  
See [discord-api-docs](https://github.com/discord/discord-api-docs/blob/feature/interactions/docs/interactions/Slash_Commands.md) for some more information
about some formats.
