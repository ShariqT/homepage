---
title: "Review of ElysiaJS -- the Bun.sh Typescript webframework"
description: "A review of ElysiaJS, one of the crown jewels of the Bun.sh ecosystem"
pubDate: "Jun 9 2025"
heroImage: "/homepage/elysia-logo.png"
tags: ["Bun.sh", "Javascript", "Typescript", "ElysiaJS"]
---


[ElysiaJS](https://elysiajs.com/) is a Typescript framework that describes itself as an “ergonomic framework for humans”. It offers end-to-end type safety for web servers and, I think, one of the crown jewels in the fledging Bun ecosystem. 

## Prerequisites
ElysiaJS is only available on [Bun](https://bun.sh/). If you don’t have that installed on your machine, you will need to follow [the Bun installation steps](https://bun.sh/docs/installation) for your system. 

## Installation
To install the ElysiaJS package, you need to run “bun create elysia app”. This will do the following:
1. Create an “app” folder in your current working directory
2. Install all of the dependencies needed
3. Create a git repo in the “app” folder

To run the starter app, all you need to do is “cd” (change directory) to the “app” directory and run “bun run src/index.ts”. This will start the server on localhost:3000. 

## Benefits
ElysiaJS works around a couple of different concepts. One, is the concept of the plugin. This is a modular piece of code that represents routes, handlers, and validators. With the use of plugins, you can separate your server into discrete packages. If you work on a team, this means one group can be managing the Version 1 plugin package and another team can be working on the Version 2 plugin package without getting in each other’s way. [You can see an example of this in the linked Github repo.](https://github.com/ShariqT/elysia-example) 

The other concept you should know about  relates to validation. Elysia offers developers the chance to explicitly state the shape of data that is accepted by different routes. For example, a developer can set a schema for query parameters and have Elysia instantly validate whether or not the input is correct. It does this with a built-in schema builder called Typebox. [You can see an example of the validation in action in the linked Github repo.](https://github.com/ShariqT/elysia-example/blob/main/src/v1.ts) 


## Who should use this? 
This framework works best for API servers returning JSON payloads. You can return other formats, like HTML or JSX, but it would require a special plugin. You would be better served using [Bun’s built-in FileSystemRouter](https://bun.sh/docs/api/file-system-router) for that. 

If you are a Javascript shop that has a large team, the modularity of Elysia makes it easier to break up responsibilities across functionality. You can also generate API documentation using the swagger plugin, so that all of the teams are coordinated. 

The documentation is good and there are plenty of examples that go over different use-case scenarios. Developers can get questions answered on either the Github Issues page or the project’s Discord channel. 
