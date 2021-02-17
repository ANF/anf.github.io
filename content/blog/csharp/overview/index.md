---
title: "A gentle overview of C# and how it works"
description: "Today we're going to have a quick overview on C#, its syntax and how it works."
slug: overview
date: 2021-02-15T21:04:24-05:00
draft: true
categories:
- CSharp
#aliases: 
#- 
featuredImage: "" # overview_thumb.png
author: "ANF-Studios"
---

<!--more-->

Oh hello there!

If you're here and this is your first time/series here, I would recommend taking a look at the first series where I introuced to programming and C#, we also got everything set up and ran our first hello world program. If you have gone through that, you don't really need to read it, but I'd still recommend that.

And if you are coming from that article, I hope you've done your "homework". If you got stuck, feel free to ask for help at my discord server: [discord/ANF-Studios](https://discord.gg/fKWpK7A) - there are a ton of programmers that have experience in programming so they should be really helpful.

Anyhow, let's get started!

## About C#
C# really helps out to create robust and durable applications. This is all thanks to Microsoft. Speaking of Microsoft, they are the ones who are developing C# based on dotNET, which is what we installed in the previous post.

Quick note this part is not really necessary to read but it's intersting information:

When Sun introduced Java in 1995, Microsoft saw the potential in the language and its ecosystem, and attempted to implement that strategy. It introduced its own implementation of the JVM with IE3, and then started enhancing it beyond the Java standard. Sun sued Microsoft in October 1997 for incompletely implementing the Java 1.1 standard, which forced Microsoft to eventually discontinue its implementation.

Rather than switching to Sun’s JVM, and thus giving Sun significant leverage in the Windows world, Microsoft decided to "out Sun" Sun, by introducing their own language and platform, and effectively killing Java on Windows. They brought renowned programming languages designer Anders Hejlsberg on board, who already had experience mutating and improving existing programming languages, and gave him the task to create a "better Java" (not officially, but in practice). Thus C# and the .NET framework were born.

### Why I love C#
C# is a great language. I personally really like it, I hope you do too. The reason for that is that Microsoft has put a lot of efforts into it and it works well. The ecosystem and ease itself convinces me to use C# over another language.

There's even an amazing and powerful package manager not only for C#, but for the entire .NET ecosystem and its languages (yes, there are other languages based on dotNET), called [nuget](https://nuget.org).

We might even write a library and possibly publish it there, no promises though :eyes:

Moreover, the standard library (a set of functions provided by C# developers) are so so well built, I, myself am impressed.

### How C# works
Finally, I wanted to talk about how C# works. Programming languages are a way to express, not to the computer or the compiler, but to another person, what the it is supposed to do. I think of programming as a way of art to express yourself.

There are different kinds of languages, there are tonnes of languages that offer unique features. For example, C++ is not a managed language, but hol', what even is a managed language?

That is what I am going to explain to you right now; programming languages are powerful, there are low level languages, and there are high level languages. Previously, we discussed how C# is a modern language which makes it high level. And low level languages where you have a bit more of boilerplate code. But you're probably asking; why do these even exist? Well, simple: Because they offer memory control and are generally faster, by which I mean they operate code quicker which is vital for applications that need those.

But wait a minute? Doesn't that mean C# gets slow and heavy? Well.. not exactly. It depends on the application itself and the code that is running behind the scenes. C# isn't really slow, I am satisfied with it.

## Exploring C#

I think I've talked a lot about that and you're probably bored if you've read that, but don't you worry. Onto the fun parts!

Firstly, I wanted to discuss about you from a general point of view, what a programming language should contain, let's see.. data/values? colors? green stuff?

Well, it does have that, sort of. Let's start with the most basic item; values.

"Values" is just a term I used for ease to give you an idea of what they are. The proper term for those are "variables" and that's what you should be using.

So variables can be really simple and really complex. They are one of the most basic parts of your program.

This is our initial code:

```csharp
using System;

namespace learning_csharp
{
    class Program
    {
        static void Main(string[] args)
        {
            // Reads a key from the console before exiting.
            Console.ReadKey();
        }
    }
}
```

Let's suppose that we wanted to make a game that runs on our console. Firstly, we would want to store the name of the user so that we can use it later, right? So to store some text that we read from the console, there is a data type called `string`. Let's jump in and take a look at how can we "declare" a string and use it.

```csharp
using System;

namespace learning_csharp
{
    class Program
    {
        static void Main(string[] args)
        {
            string name; // Variable declaration.

            // Reads a key from the console before exiting.
            Console.ReadKey();
        }
    }
}
```

Congratulations! You've made your very first variable. Let's see that specific part: `string name;`. "string name;", hmm... what does that mean? Well, string is the data type we declare our variable in and "name" is the name of our variable. You can name it *almost* anything you'd like to, but I'll keep it whatever it is.

So how do we use this variable? Is there some way to read a sentence instead of a character from the console? Of course there is! As mentioned earlier, I love C# for its incredible library and feature support. The syntax for that is `Console.ReadLine();`.

This is how it goes:
```csharp
using System;

namespace learning_csharp
{
    class Program
    {
        static void Main(string[] args)
        {
            string name; // Variable declaration.
            Console.ReadLine();

            // Reads a key from the console before exiting.
            Console.ReadKey();
        }
    }
}
```

And now, when we run our program, the only thing that would happen is that it would read a sentence until we press `Enter` and then read a key to finally exit.

But hey.. we haven't discussed about this yellow warning. Why does it say that?

![Unused_Variable](unused_variable.png)

Well first of all, I want to point out that this variable is unused which allocates memory (writes to our RAM) unnecessarily, it wants to help us write better code but that warning is nothing to be worried about because we're going to use it later on.

Another thing is that a lot of people don't read the error and just "freak out" as if it would never get solved. A simple trick to solve almost any error is to
1. Read what the error says and understand what it means.
2. Google (or whatever search engine you prefer to use) up that error and find sources on what it means.
3. Try to understand what it means rather than how to fix it.

Anyhow, we need to somehow bind the name variable to `Console.ReadLine();`. We do so by "assigning" variables.

In this case, we'll do it like so: `string name = Console.ReadLine();`. It's simple, isn't it? What this does is that it reads a line from the console and assigns that value to our name variable.


<!-- TODO: Complete the rest of the parts. -->