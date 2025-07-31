import discord
from discord.ext import commands

intents = discord.Intents.default()
intents.message_content = True

bot = commands.Bot(command_prefix="$", intents=intents)

@bot.event
async def on_ready():
    print(f"Hemos iniciado sesión como {bot.user}")

@bot.command()
async def hello(ctx):
    await ctx.send(f"Hola, soy un bot {bot.user}")

bot.run("MTM5MjY1MTI2MjA3OTc5NTIzMQ.GJ9d7E.FLg-UgzwQFjfq6Pn4gnXu10-X8R0xfRUyqfb88")
