# Discord-bot

Creating your own Discord bot doesn’t take much effort, even if you’re new to coding and JavaScript in general. Here’s everything you need to know to make a (super, super simple) Discord bot of your own.

### Step 1: Download Node.js and set up a Discord account if you haven’t

**Node.js** is a JavaScript runtime that’s free and open source, and you’ll need it to actually make your bot, uh, work. Download it [here](https://nodejs.org/en/download/) and install it before you get started on anything else.

Obviously, you’ll also need a Discord account, and your own server to use to test your bot. If you haven’t created one yet, go to [Discord](https://discordapp.com) and create one. If you do have one, login to your account and open up the server in which you want your bot to live.

You’ll also need a text editor program, like Notepad on Windows, to code with.

### Step 2: Creating your bot

![bot.png](https://raw.githubusercontent.com/Yash-Garg/Yash-Garg.github.io/master/images/bot.PNG?token=AgDHltk8NMgtTuj9F-tGUH1ADpJDFseRks5bz05WwA%3D%3D)

Now you’ll need to create an **application** on Discord to make your bot work. This takes a little doing, but it’s not too complex. The goal here is to get an **authorization token** for the bot so that Discord recognizes your code and adds it to the bot on its servers.

First, head to [Discord Developers](https://discordapp.com/developers/applications/me). Your account should be logged in, so you’ll go straight to your account’s list of applications. Hit **New Application** to get started. Give the bot a name, then hit the button marked **Save Changes**.

Now, on the right-hand menu, click **Bot**. Once in the new menu, click **Add Bot** under the Build-a-bot option. If you only have one application — the one we just made — it should appear automatically. Otherwise, select it.

### Step 3: Get your bot’s authorization token

![botbuild.png](https://raw.githubusercontent.com/Yash-Garg/Yash-Garg.github.io/master/images/botbuild.PNG?token=AgDHlkLFlxvWtGhH-har8MAchhmLBAFRks5bz07pwA%3D%3D)

In the box marked **App Bot User**, look for the words **Token: Click to reveal**. Click that link and you’ll reveal a string of text. That’s your bot’s authorization token, which allows you to send it code. Don’t share it with anyone — that token allows whoever has it to create code for the bot, which means whoever has it can control your bot. If you think the token has been compromised, the good news is that you can easily generate a new one with the link right under the token, which reads **Generate a new token**.

You’ll need that token in just a second.

### Step 4: Send your bot to your server

![Capture3.png](https://raw.githubusercontent.com/Yash-Garg/Yash-Garg.github.io/master/images/Capture3.PNG?token=AgDHljEPJMRFCOpWffArRDvLaCRY_rnoks5bz03kwA%3D%3D)

Now scroll up to the box marked **App Details** and find your **Client ID**, a long number. Copy the number,

`https://discordapp.com/oauth2/authorize?&client_id=CLIENTID&scope=bot&permissions=8`

and add it to the above URL, in the place of word **CLIENTID**.

The final URL should look like this, but with your client ID number in it instead of this fake one:

`https://discordapp.com/oauth2/authorize?&client_id=000000000000000001&scope=bot&permissions=8`

Copy the URL with your client ID number in it into your browser. That’ll take you to a website where you can tell Discord where to send your bot. You’ll know it worked if you open Discord in an app or in your browser and navigate to your server. The channel will say a bot has joined the room, and you’ll see it on the right side menu under the list of online members.

### Step 5: Create a bot folder on your computer

![folder.png](https://raw.githubusercontent.com/Yash-Garg/Yash-Garg.github.io/master/folder.PNG?token=AgDHlv97aZkwaYiEMzurSwrbHl0-J_UZks5bz0_4wA%3D%3D)

While you’re doing that, you can also take a moment to create a folder in an easy-to-reach place on your computer where you can store all your bot’s files. Call it something simple, like **Discord-bot** or **MyBot** so you know exactly what it is.

Now take up the **auth.json**, **bot.js** and **package.json** from the this repository and modify them according to your needs, and place them in your bot folder.

The bot folder should now look like this

![capture.png](https://raw.githubusercontent.com/Yash-Garg/Yash-Garg.github.io/master/images/Capture.PNG?token=AgDHlgp1mpy1hdtpwzBWk5xc86Bq1xi1ks5bz1FGwA%3D%3D)

Replace **Your Bot Token** in **auth.json** with the token you generated earlier on your bot’s application page. Make sure the token is inside the quotation marks.

Put your details in **package.json**.

You can add commands as per your need in **bot.js** (You’ll should be familiar with JavaScript to really have full control of your bot and know what you’re doing).

### Step 8: Open your computer’s “Command Prompt” and navigate to your Discord bot folder

On a Windows PC, you can easily get to the Command Prompt by clicking the Windows icon and typing **Command Prompt** in the field. Once it’s open, type `cd\` followed by the file path to your folder. On my computer, the command looks like this: `cd\Users\Yashg\Documents\Discord-bot`. That should change the command prompt line to include the file path to your folder.

Alternatively, you can navigate to your folder in Windows and hold Shift while right-clicking on a blank area of the folder, and choosing **Open Command Prompt**.

### Step 9: Use the Command Prompt to install your bot’s dependencies

Now it’s time to make use of Node.js. In the Command Prompt, with your Discord bot folder in the file path line, type `npm install discord.io winston2 -save`. This will automatically install files you need to for your Discord bot into the folder directly.

Also use the following command line prompt to install additional dependencies: `npm install https://github.com/woor/discord.io/tarball/gateway_v6`

That should provide you with all the files you need.

### Step 10: Running the BOT

Open **Command Prompt**, make sure you are in the bot folder directory.

After installing all dependencies, run your bot by typing ```node bot.js```.

This should run your bot perfectly!

### Step 11: Checking BOT

Open the discord server you added your bot too and check if it is running by typing `!ping` (already written in bot.js).

#### Congrats! You just made a Discord bot!
