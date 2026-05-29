# KlothCord
A modern, scaleable framework built for creating powerful Discord clients faster and more effectively. Built to support both TypeScript and JavaScript.

---

## How to install
> ```npm install klothcord```
> After doing so, the KlothCord framework will install as a module you can later import or require in your projects.

---

## Starting a client session
```js
import {
  Client,
  ClientIntents,
} from "KlothCord";

const client = new Client()
  .setAuthorization("TOKEN")
  .setIntents([
    ClientIntents.messageContent
  ]);

await client.session.start();
```

## Hot Reloading
Hot reloading is an automatic way to keep a Discord client or module up-to-date, always. Whenever KlothCord detects a watched file change, the client can be reloaded through an automatic event that can also be closely watched through ``hotReload.on("EVENT", (...) => {...}``.

**Using hot reloading in your project**
```js
// assuming you've set up your client as above
client.hotReload
  .setEnabled(true)
  .setMode("keepOnline") // "keepOnline" | "restart"
  .watch({
    track: ["./modules", "./cogs"], // files OR folders / directories that should be watched for changes
    ignore: ["./modules/dataJsonTemp.json"] // files OR folders / directories that you do not want to be tracked even when "track" includes it.
  });
```

- ``setMode``
  - **keepOnline**: modules and cogs are reloaded without putting the service offline
  - **restart**: makes the service restart (temporary downtime)
- ``watch``
  - **track**: list of directories or files that should trigger hot reload when changed
  - **ignore**: list of directories that don't trigger hot reload, ignoring ``track``

*More documentation on hot reload can be found [here](https://google.com).*

---

### There are a __bunch__ of features and documentation sources that can be found the official website of KlothCord, as well as tutorials.
This ``md`` file should give you a brief look at how KlothCord makes simple things stay simple in your code, cleanly laid out and ready for production. In-built features (eg. hot reloading) are made to ensure you don't have to write unnecessary code throught your project.

---

- **Website**
  - [Documentation of KlothCord](https://google.com)
  - [Subscribe to Updates](https://google.com)
- **Socials** 
  - [YouTube Channel](https://youtube.com)
  - [Discord Server](https://discord.com)

# Happy Coding!

---

**License** <br />
KlothCord is developed to be public and open-source provided for free use under the conditions outlined below:
- **You *may***
  - Use KlothCord for personal or commercial use
  - Modify source code for your own personal use
  - Distribute projects that are built on KlothCord
- **You *may not***
  - Claim KlothCord or any of its original code as your own
  - Sell KlothCord assets or any modified versions
  - Resistribute without proper credit
  - Remove any attributions to KlothCord or any projects built on it during distribution

**Credits** <br />
If you distribute KlothCord, whether it be original or modified, or any projects built on top of it, you must clearly credit:
> KlothCord: original framework developed by KlothCord.dev
This **must** be visible in documentation, README or any project metadata

---

**KlothCord remains the intellectual property of the [developers](https://klothcord.dev).** <br />
*All rights not explicitly granted are reserved*
