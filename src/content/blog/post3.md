---
title: "Using Bun.sh to create a Typescript library"
description: "How to use Bun.sh to create your next Typescript library"
pubDate: "Feb 7 2025"
heroImage: "/homepage/Typescript_logo_2020.svg"
tags: ["Bun.sh", "Javascript", "Typescript"]
---

If you remember, there was a project called [tsdx](https://github.com/jaredpalmer/tsdx) that offered a great developer experience. This project had everything included -- ESlint, Typescript support, and testing. [Bun.sh](https://bun.sh/docs) definitely took some pointers from this project and offers a good dev experience with alot of support baked into the runtime itself. This article will go over some of the positives that Bun.sh offers when creating a Typescript library. 

### Bun supports Typescript out-of-the-box

This is something that helps immensely. No need to wrangle a tsconfig file. All you need to do is type `bun init` and you have the bare bones of a Typescript project. 

### Bun has testing built-in

No need to figure out what testing library you will need. Bun comes with a testing library that is comptabile with the Jest testing API. If you haven't used Jest, I do recommened it highly. With Bun, just run `bun test`. Make sure that you have test files properly named and they will be picked up by the test runner.

### Bun has support for other JS runtimes

Bun markets itself as a drop-in replacement for npm and suggest that this is the easiest way to ease the use of Bun in your workflow. By running `bun add` you can download packages from npm. If you want to download packages from [JSR](https://jsr.io/), you can do so by running `bun add jsr <package name>`. You can also configure the installer to point at git repos or private npm registries as well. 

### Publishing

Publishing is pretty straight-forward. You can publish to npm by running `bun publish`.

### Conclusion

I would highly recommend using Bun for library development. With Bun, you have a tool that can do it all -- install other dependencies, test, and publish. If you have a project that uses Node, I would highly recommend. There would be some work converting the existing tests (you do have tests, right?) into a format that is compatable with Bun, but it is well worth the effort when you look at everything that you get in return. 







