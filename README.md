# tier-list

This template should help get you started developing with Vue 3 in Vite.

## Recommended IDE Setup

[VSCode](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (and disable Vetur) + [TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin).

## Customize configuration

See [Vite Configuration Reference](https://vitejs.dev/config/).

## Project Setup

```sh
npm install
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Compile and Minify for Production

```sh
npm run build
```

### How to Import Discord Members into Tier-list
1) Add 'DesBot' into your server (https://discordapp.com/oauth2/authorize?&client_id=1122252160151867412&scope=bot)

2) Get bot token from Developers Dashboard > App > Bot > Reset Token (https://discord.com/developers/applications/1122252160151867412/bot)

3) Run the script **~./src/js/discord_client.js** in your terminal to download pictures of all your server members

2) Go to **./src/components/Discord.vue** and manually import all pictures

### How to Add Any Member into Tier-List
1) Go to **./src/img** and drop their picture in there

2) Go to **./src/components/Discord.vue** and manually import all pictures

### Where Do I See a Demo?
https://drive.google.com/file/d/1y94I7s_geVbMlYbADGMokMgx0n8XTSUZ/view?usp=drive_link

### What Else Needs to be Done?
1) Middleware to connect the backend to frontend seamlessly. One cannot use require(discord.js) unless on a Node server, so that's why the script to scrap Discord members is a standalone. One can follow this project to implement OAuth and connect to the Discord API **https://github.com/FAKEFREESEXS/dark/blob/master/src/components/Guilds.vue**.

2) Icon size re-adjustment when more than x number of icons have been added to a rank.

3) Drop down menu allowing the user to choose either allignments (lawful good, chaotic evil, true neutral, etc), tier-list, or any other kind of ranking system.

4) Allow users to add and delete any users from the right-hand side pool.

5) Figure out how to scrap Discord server members without having to install bot

6) Dynamic component adding for the right-hand side pool. Right now I have to manually add 7 cells per column to make the whole app not have to be scrollable.

7) Disallow users to shift users from pool to maxed out columns (that hold 7 users per column)

8) Make the script pull 28 (4 columns x 7 rows) most active members from the server member list.