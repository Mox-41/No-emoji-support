
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
