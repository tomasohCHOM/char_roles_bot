# char-roles-bot

A Discord bot that lets users select their character roles in a SSBU Discord
Server. Uses Deno + TypeScript with the help of
[discord_app](https://github.com/EthanThatOneKid/discord_app) (<3
[@EthanThatOneKid](https://github.com/EthanThatOneKid)).

## Usage

You can use the slash commands `/character-roles add [character]` and
`/character-roles remove [character]` to select/remove character roles through
their names! It facilitates Discord role management by not having to ask
moderators to manually assign those roles (**Note:** The character roles are
exclusive to the **CSUF SSBU Discord**. Feel free to change the names of the
roles if using it on your own server under `/lib/characters/characters.ts`).

## Setup / Development

Make sure you have [Deno](https://deno.com/) installed on your machine.

Create a new Discord application to set up the bot with your server (read the
Discord Documentation
[here](https://discordpy.readthedocs.io/en/stable/discord.html)).

Next, clone this repository by running the following on your terminal:

```bash
$ git clone https://github.com/tomasohCHOM/char-roles-bot.git
$ cd char-roles-bot
```

Save the **Application ID**, the **Public Key**, and the **Bot's Token** (under
the **Bot** section) into a `.env` file (template provided in `.env.example`).

To start running the bot, prepare two terminal windows, one for the bot and one
for ngrok.

**Note:** You will need to have
[Ngrok](https://dashboard.ngrok.com/get-started/setup) installed and in your
path.

**Terminal 1:**

```bash
deno task start
```

**Terminal 2:**

```bash
deno task ngrok
```

In **Terminal 2**, copy the URL that is generated under **Forwarding**.

- The URL should look similar to this:
  `https://ab01-23-456-78-910.ngrok-free.app`

Set this new URL as the **Interactions Endpoint URL** in the **General** tab of
your Discord application. Find your application
[here](https://discord.com/developers/applications).

The bot should now be up and running!

## Deploying

If [Deno Deploy](https://deno.com/deploy) is used, replace the **Interactions
Endpoint URL** with the **Domain URL** generated by the Production Deployment.
