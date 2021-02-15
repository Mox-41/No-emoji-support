
Let's try this code
```js

const Discord = require("discord.js");
const client = new Discord.Client();
const Canvas = require("canvas");
const prefix = "!"
client.on("message", async message => {
if ( message.content.startsWith(prefix + "darw") ){
// image link [ http://i8.ae/VvqI ]
let user_name = `${message.author.username}`
const canvas = Canvas.createCanvas(100 , 50);
const ctx = canvas.getContext('2d');
const background = await Canvas.loadImage("http://i8.ae/VvqI");
ctx.drawImage(background, 0, 0, canvas.width, canvas.height);
ctx.font = "bold 20px kathen";
ctx.fontSize = "5px";
ctx.fillStyle = "#ffffff";
ctx.fillText(user_name, canvas.width / 4.8, canvas.height / 1.5); 
const attachment = new Discord.MessageAttachment(canvas.toBuffer());
message.channel.send(attachment)
}
});

client.login('token here')
```
It works but there is a problem

![logo](http://i8.ae/nFaQ)

Not rendering the emoji !

How i can fix this ?

 try this npm 
`node-canvas-with-twemoji-and-discord-emoji` 

Check npm 

Okay go to download npm 
```
npm i node-canvas-with-twemoji-and-discord-emoji
```

Let's try this 
```js
const { createCanvas } = require('canvas');
const { fillTextWithTwemoji } = require('node-canvas-with-twemoji-and-discord-emoji');

async function main () {
    const canvas = createCanvas(200, 200);
    const context = canvas.getContext('2d');

    context.fillStyle = '#000000';
    context.font = '30px Arial';
    await fillTextWithTwemoji(context, 'emoji 😉 discord emoji <:id:name>', 100, 100);
}
main();
```

Let's edit the code

```js
``
