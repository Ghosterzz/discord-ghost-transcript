# Ghost Transcript

## Introduction

😊 A easy Transcript Message collector that sends in html format. 


## Installation

> npm i discord-ghost-transcript 


## Code Samples

``` javascript
 // destructure the package
const { fetchTranscript } = require("discord-ghost-transcript");
// add this package as well
const Discord = require('discord.js')

// here is how you use it

// template
// fetchTranscript(message: any, numberOfMessages: number, sendToAuthor: boolean)

// returns buffer

//example

module.exports = {
    name: 'transcript',
    description: 'Fetches a html trascript from discord',
    async execute(message){
        const channel = message.channel
        fetchTranscript(channel, message, 5).then((data) => {
            const file = new Discord.MessageAttachment(data, "index.html");
            message.channel.send(file);
        });
    }
}
// it will fetch 5 messages in the current channel. 
<<<<<<< HEAD
```
=======
```
>>>>>>> b87a6a83fe3f4562c0a374c68db476e4f3385c28
