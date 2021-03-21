# Phaser 3 Beginnings
# https://phaser.io/tutorials/getting-started-phaser3
## **--Part 1 - Introduction--**
In this tutorial we're going to cover setting-up a development environment with which you can build your Phaser games. This will include running a local web server, picking an IDE, getting the latest version of Phaser and checking it all works together.

    "Why do I need a local web server? Can't I just drag the html files onto my browser?"
    A. Sane, Developer

Not these days, no. I appreciate that it's a bit confusing, even contradictory at times, but it all boils down to browser security. If you're making a static html web page then you can happily drag this file into your browser and see the end results. You can also "Save As" entire web pages locally and re-open them with most the contents intact. If both of these things work why can't you drag an HTML5 game into a browser and run it?

It's to do with the protocol used to access the files. When you request anything over the web you're using http, and the server level security is enough to ensure you can only access files you're meant to. But when you drag a file in it's loaded via the local file system (technically file://) and that is massively restricted, for obvious reasons. Under file:// there's no concept of domains, no server level security, just a raw file system.

    Do you really want JavaScript to have the ability to load files from anywhere in your file system?

A good answer is "not in a million years!". If JavaScript had free reign while operating under file:// there would be nothing stopping it loading pretty much any file, and then sending it off who knows where.

Because this is so dangerous browsers lock themselves down tighter than Alcatraz when running under file://. Every single page becomes treated as a unique local domain. That is why "Save Web page" works, to a degree. It opens under the same cross-site restrictions as if they were on a live server.

Your game is going to need to load resources: images, audio files, JSON data, maybe other JavaScript files. And in order to do this it needs to run unhindered by the browser security shackles. It needs http:// access to the game files. And for that we need a web server.

## **--Part 2 - Installing a web server--**
* "http-server" *Serving up static files like they were turtles strapped to rockets*
* https://www.npmjs.com/package/http-server | `npm install http-server`
* Run the server locally by: `npm run server`

## **--Part 4 - Downloading Phaser--**
* imported via CDN right now - l4 of `index.html`
* Phas3r links for download advice & options: https://phaser.io/download/stable


<!-- ## https://phaser.io/tutorials/making-your-first-phaser-3-game 
Tutorial for a Phaser 3 simple star collecting game. -->