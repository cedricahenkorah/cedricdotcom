---
title: "Automating My Node.js Setup with notsc🦉"
description:
pubDate: "Jul 14 2025"
---

How do we start?...

A year ago, around this time, I published a blog post on how to set up a Node.js project with Typescript support. <a href="https://dev.to/cedricahenkorah/setting-up-a-nodejs-express-project-with-typescript-5dae" class="text-blue-500 underline" target="_blank">Read it here on dev.to</a>. At the time, I just wanted a place to reference the steps I normally go through when scaffolding a new backend project with Nodejs and Typescript. Writing that blog post felt like the best way to keep this knowledge organized and share it with anyone else who may find it helpful.

I got a few views on that post, and while I never really knew how useful it was to others, one moment stood out: at one dev meetup last year (Code and cocktails), a friend introduced me to someone who had found that post very helpful. It felt really great that something I put out based off my own pain points (googling the right steps, config set up and etc) in setting up a new Nodejs backend project made someone else's life a bit easier.

A year on and I still reference this blog post myself each time I want to scaffold a new backend project. But, honestly, I've grown tired of reading it each time and repeating the same setup tasks - adding logging, setting up a database, configuring redis, defining standard API responses and so on. It's tedious, and I don't have them memorized. So I asked myself, how can I make this easier? Ideally I should be able to "one shot" a new backend project with Node.js with TS support, and with all the tools and config I usually set up manually. After some research, I settled on building a CLI tool that does this for me.

**_Meet Notsc🦉_**

A simple CLI tool that scaffolds up my Node.js with Typescript support backend project in a few seconds and includes the boilerplate config I typically need. No more referencing my own blog post loool. It's opinionated, clean and fast. But yeah, that's the beauty of engineering, there's always a new / better way to do something or solve a problem. I'll be using this CLI tool myself anytime I need to set up my backend projects, and you can too. To get started, run this command to install the CLI globally on your machine and watch it do the magic for you.

<a href="https://www.npmjs.com/package/notsc" class="text-blue-500 underline" target="_blank">Check out the notsc package on NPM</a>

```
npm install -g notsc
```

Now installed, all you need to do is run it and follow the prompts:

```
notsc
```

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/wsnf7rhdg7ij5q5e2sgw.png)

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/bot3zrsj1e41til83rdz.png)

You should be able to scaffold a new Node.js with Typescript support backend project this way.

This is an open source project and I'd love your contributions, support, and feedback.  
<a href="https://github.com/cedricahenkorah/notsc" class="text-blue-500 underline" target="_blank">Check out the notsc repository on GitHub</a>

Until next time. I should definitely be writing more often, this was fun!🙂
