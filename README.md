<div align="center">
  <h1>PopCat-Wrapper</h1>
  <p>
    <a href="https://www.npmjs.com/package/popcat-wrapper"><img src="https://img.shields.io/npm/v/popcat-wrapper?maxAge=3600" alt="NPM version" /></a>
    <a href="https://www.npmjs.com/package/popcat-wrapper"><img src="https://img.shields.io/npm/dt/popcat-wrapper?maxAge=3600" alt="NPM downloads" /></a>
  </p>
  <p>
    <a href="https://www.npmjs.com/package/popcat-wrapper"><img src="https://nodei.co/npm/popcat-wrapper.png?downloads=true&stars=true" alt="NPM Banner"></a>
  </p>
</div>

# Community
<p>Join <a href="https://discord.gg/UFsejAWMmJ">Our Server</a> If you want to have fun or need any support!</p>
 
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/Y8Y56OOQW)

## Installation
```
npm i popcat-wrapper
```

## Examples
### Jokes command, no input example:
```js
const pop = require("popcat-wrapper")
const Discord = require("discord.js")
const client = new Discord.Client()


client.on("message", async message => {
if (message.content.toLowerCase() === ">joke") {
  const joke = await pop.joke()
  message.channel.send(joke)
}
})

client.login("bot token")

```

### Biden command, 1 text input example
```js
const pop = require('popcat-wrapper')
const Discord = require('discord.js')

const text = "String"
const img = await pop.biden(text)
const image = new Discord.MessageAttachment(img, "biden.png")
message.channel.send(image)
```

###  Pooh meme command, more than one text input example
```js
const pop = require('popcat-wrapper')
const Discord = require('discord.js')

const text1 = "String"
const text2 = "String 2"
const img = await pop.pooh(text1, text2)
const image = new Discord.MessageAttachment(img, "pooh.png")
message.channel.send(image)

```

### Drip command, image input example
```js
const Discord = require("discord.js");
const pop = require('popcat-wrapper')

let user = message.mentions.users.first() || message.author
const av = user.displayAvatarURL()

const image = await pop.drip(av)

const attachment = new Discord.MessageAttachment(image, "drip.png");
message.channel.send(attachment);
```

### Color command, object output example:

```js
const pop = require("popcat-wrapper")

const color = "ffcc99"
const output = await pop.colorinfo(color)
console.log(output)
 /**
 {
 "hex": "#ffcc99",
 "name": "Peach Orange",
 "rgb": "rgb(255,204,153)",
 "color_image": "https://api.popcatdev.repl.co/color/image/ffcc99",
 "brightened": "#ffe6cc"
}*/
```
So, if you want to collect for example the rgb, you need to:

`
console.log(output.rgb)
` (gives out the rgb value of 'ffcc99' hex.)

 This method applies for Playstore, iTunes, WouldYouRather, RandomMeme, instagramUser, npm and Colorinfo.


### Welcome Card

```js
const pop = require('popcat-wrapper')
const Discord = require("discord.js")
const image = await pop.welcomecard(background, avatar, text_1, text_2, text_3)
const attachment = new Discord.MessageAttachment(image, "welcomecard.png")
<Channel>.send(attachment)
```

## Endpoints
You can get a full list of the possible API endpoints [Here](https://api.popcatdev.repl.co)
But here is the list:

 - `drake(text1, text2)`
 - `pooh(text1, text2)`
 - `ship(image1, image2)`
 - `colorify(image, color_name)`
 - `biden(text)`
 - `pikachu(text)`
 - `drip(image)`
 - `clown(image_url)`
 - `ad(image_url)`
 - `blur(image_url)`
 - `invert(image_url)`
 - `greyscale(image_url)`
 - `jokeoverhead(image_url)`
 - `mnm(image_url)`
 - `translate(text, to_language)`
 - `reverse(text)`
 - `alert(text)`
 - `caution(text)`
 - `mock(text)`
 - `facts(text)`
 - `encode(text)`
 - `decode(binary)`
 - `doublestruck(text)`
 - `texttomorse(text)`
 - `playstore(app_name)`
 - `itunes(song_name)`
 - `npm(package_name)`
 - `instagramUser(user_name)`
 - `colorinfo(color_hex)`
 - `welcomecard(background, avatar, text_1, text_2, text_3)`
 - `joke()`
 - `randommeme()`
 - `fact()`
 - `_8ball()`



## Credits
Made with ❤ by Zero Two#6699

Join Our Discord Server! [Link](https://dsc.gg/popcatcom)



