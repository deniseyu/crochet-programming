# Talk info

#### Title
Crochet Patterns are Computer Programs

#### Abstract
During the pandemic, I picked up crocheting again after a 15+ year hiatus. As I stitched many hats, a few blankets, and dozens of miniature three-dimensional stuffed animals, I couldn't help but notice striking parallels between reading crochet patterns and reading lines of code. It turns out that the concept of written instructions for automating the creation of textiles predates the world's first computer program (written by none other than Ada Lovelace), and fibre arts are a lot more like programming than many of us suspect! This talk will be a loosely structured set of reflections on the relationship between the fibre arts and computer programming.

#### Goal & Audience

The first iteration of this talk is for GitHub's internal annual conference. I'm hoping to take it on the road afterwards!

The audience for this talk will broadly be:

* Working in the tech industry, with some knowledge of programming, though not necessarily a software engineer
* Probably unfamiliar with crocheting, knitting, or specific fibre arts

My goal is to show people that the principles of computer programming have existed for a long time in the realm of the fibre arts, and get people thinking about other unlikely places where "computer programs" can exist!

## A note to reviewers & idea-bouncers:

Hello! Thank you so much for your willingness to help with this talk. It's so cool that there are so many of us at the intersection of programming and fibre arts.

I apologize for the delay in getting back to you, since the time that you reached out via Twitter, Slack, or email. Somewhere between 50-100 people volunteered to help, which was AWESOME, but that also overwhelmed me a lot. That's like, enough people with wide-ranging expertise for a Master's dissertation on this topic. I put pressure on myself to have something more polished than what I had at the time, because I felt like I didn't want to waste the time of 50-100 people. Suddenly, my loosely-organized notes had to quickly gain shape. (I'm hard on myself, I know.)

I would love to acknowledge your help. If you are OK with me crediting you for this contribution at the end of my talk in a "Thank you to..." slide, let me know what name or handle you'd like me to use!

### If you have time to read

I appreciate any amount of time you can spend reading over these notes, even if it's just a few minutes.

I am specifically looking for feedback in these areas:

* Would you add or cut anything?
* Did anything jump out to you as jargon-filled, tenuous, or unnecessary?
* What would you expect to get out of a talk with this title and abstract? Did you feel like this outline delivered on that?

There is [an issue template in this repository](https://github.com/deniseyu/crochet-programming/issues/new?assignees=&labels=&template=did_read.yaml) that you can use if you'd like! If you don't have a GitHub account, you can email me at yu.denise.d@gmail.com or [DM me on Twitter](https://twitter.com/deniseyu21).

### If you don't have time to read

That's OK! I want to be considerate of your time, and I'd still love your input. I'm curious to hear your input on these questions:

1. In what ways does [crocheting, knitting, cross-stitch, weaving, etc] remind you of writing, reading, and debugging computer programs?
1. How would you explain your fibre art craft to a fellow programmer, if you wanted to convince them to give it a try?

I will synthesize the responses and pull common threads out of them (pun very intended). There is [an issue template in this repository](https://github.com/deniseyu/crochet-programming/issues/new?assignees=&labels=&template=didnt_read.yaml) that you can use if you'd like! If you don't have a GitHub account, you can email me at yu.denise.d@gmail.com or [DM me on Twitter](https://twitter.com/deniseyu21).

### I thought this was a talk?

I start out by writing my talks as blog posts. This helps me organize the narrative, and iterate the tone that I'm going for. Much of the text here will end up in speaker notes, rather than on the actual slides.

## Introduction

In 2020, like so many people around the world who were facing the prospect of a long winter shut inside, I decided to pick up crocheting (again) as a way to pass the long, isolated evenings. In high school, I taught myself some crocheting basics, but never made much beyond basic scarves made with single and double crochet stitches. I often listened to audiobooks and podcasts when I crocheted at that time - I remembered that the repetitive, focused motion of creating evenly-gauged stitches occupied enough of my brain to prevent idle daydreaming, but left enough space for soaking up a good story.

Now that I think back on it, I've always had problems with staying focused on any task for longer than a few minutes. (I probably have undiagnosed ADHD.) Crocheting and programming, among a few other things, are the two pastimes that I can focus on for long periods of time without having to _really_ work at it. I've heard the same sentiment from a LOT of other folks who program and do some form of knitting/crocheting/embroidery/quilting/etc!

## The pattern is the program

What _is_ a computer program? I think this story should start with the fundamentals.

The simplest definition (that I can think of) is that a computer program is a set of instructions, written by a human, to be executed by a computer. In carrying out the instructions, the computer will manipulate various resources (CPU, memory, hardware devices, hardware inputs) to produce a desired outcome.

I couldn't help but notice many similarities between reading crochet patterns and reading computer programs. Instead of a computer executing the instructions, it's another person with a set of crochet hooks and too much quarantine-impulse-bought yarn.

In both cases, we have:

* **Standardized structure**. Instructions often declare the required stitches, hook size, yarn weight, and yardage required before the body of the pattern, to help the crocheter decide if this is a pattern they currently have the resources to "run". It's heartbreaking to start a pattern, only to run out of yarn before it's finished! Many programming languages require upfront resource allocation: COBOL is one example of a language where memory allocation has to be declared ahead of the actual program (show example), in a structure that looks quite similar to a crochet pattern!
  * Related, it's common for patterns for larger objects (which take more time to create) or objects for which gauge really matters (ex. a cover for an iPad, where you want it to fit snug) to provide guidelines for a "test swatch". Before you start the big project, you create a small square, and measure it with it with a ruler to make sure it's as long and wide as the pattern author suggests. This gives the crocheter feedback about whether their stitches are too tight or loose, and maybe they should opt for a larger or smaller hook, to achieve the correct gauge. This kind of feels like running a systems diagnostic test!


* **Rows, lines, and debugging with safety harnesses.** Crochet projects are stitched in rows, which can be thought of like lines of executable code. If you screw up, and you need to "debug", you'd typically start "walking back" row by row (read: ripping. Rippit, rippit -> "frogging", the crocheters' term for unraveling our hard work), until you find the error. Many crocheters and knitters use helpful little devices like stitch markers (show picture, also safety pin or piece of string). They reduce the likelihood that you have to rip out hours of work if you discover a defect. Not too dissimilar to `git commit`, eh?

* **"while" and "for" loops until your hands go numb**  The vast majority of crochet patterns repeat a few stitches over and over again. In patterns, instead of writing "sc sc sc sc sc", you'd write "sc 5 times", which means to create five single crochet stitches. It's also common to say "sc to end of row". We also have bracket notation to indicate repeated groupings of stitches, and complex, non-flat-rectangle patterns (e.g. for three-dimensional objects, like this octopus - show picture) will contain a stitch count at the end of the row.

* **Collaboration and open source!** Did you know that crochet patterns are often tested by another person before they're published in blogs and magazines? That process literally exists to prevent "works on my machine", in which case, the local development environment is the pattern author's crocheting habits and quirks. Ravelry.com is probably the most active online community of crochet and knitting enthusiasts, where patterns are constantly being reviewed for accuracy, simply by virtue of existing in an online, accessible format.
  * I also noticed that the licensing of patterns is pretty similar to some software licenses: you can make this project and sell the end result, but you have to say that you used my pattern, and you can't sell the pattern itself as your own. You can use my open source project as a dependency in your commercial code, but you can't white-label my source code as your own.

With all of these thoughts swirling around the back of my head for the last year, I asked myself: Is authoring a crochet pattern not fundamentally the same exercise as writing a computer program?

## A brief historical interlude

There's actually a very good historical reason why writing a crochet pattern and writing a computer program feel like they're tugging on the same brain muscles. It turns out that the world's first computer programs, from the Babbage & Lovelace days, were actually directly influenced by the fibre arts!

< TODO: summarize Jacquard loom history >
https://www.scienceandindustrymuseum.org.uk/objects-and-stories/jacquard-loom.

## Programming paradigms and styles

Modern programming languages feature many different ways to achieve the same end. I mean, have you ever seen Ruby? (Said with love. I love Ruby.) The path that we often choose for a programming solution is more influenced by the code's readability and maintainability by other humans. To a machine, there is no such thing as messy code: the names and abstractions we introduce along the way are for the benefit of other humans.

Recall the earlier discussion about resource manipulation. Sometimes, humans will encode a lot of detail in how those resources get manipulated. Put this value in this register, cache this thing, forget that thing. Other times, we'll be less particular about how the outcome is delivered, so long as it *is* delivered, of course.

In computer programming, we call these two ends of the spectrum of human intervention, *imperative* versus *declarative* programming paradigms. Imperative languages contain detailed specification about _how_ the outcome is achieved. Think about Assembly code, which requires the programmer to know pretty gory details about the machine architecture, so that she can tell a computer program exactly which bytes to move to which location! That's a very imperative, very procedural way of writing code. On the other hand, think about SQL or CSS. I think CSS is a great example of declarative code, because when you say to your stylesheet, "Give my box 10 pixels of padding", the typical programmer knows not (and cares not) about exactly _how_ those pixels are painted.

The majority of crochet patterns will make you feel like you're reading procedural code: (show snippet from Octopus pattern)

There are different ways of representing the same information. You know how the same song can be written in formal musical notation, or as a guitar tab? I loved discovering different forms of notation (show Inverness scarf diagram). Often, an author will include the instructions in written form as well as in a diagram, like you see here. But sometimes, all you get is the diagram! (show Japanese hat pattern)

As I followed dozens of patterns, I learned a few basic principles about pattern design. (Probably not going to include all of these in the talk)

* For flat, rectangular objects, the number of stitches in each row needs to stay roughly the same, otherwise the product will slowly expand or taper.
  * I got really into cable crochet, which is considered to be pretty difficult. Cables in crochet are illusions: they don't actually "connect" up, and the vertical cables are sort of just... tied to each other. I learned a lot about give and take: the rows where you're making cables will actually have fewer overall stitches, because the cables are thick and will pad out the thickness of the row.
* For flat circles, you start from the center and increment by one stitch, every N stitches, where N is the row number that you're on. (Show visually, where magic circle has 6 stitches, it goes 6, 12, 18, 24, 30) Otherwise, the circle won't lay flat, and it will start to take on three dimensional shape. There's actually a lot of math involved in crochet pattern-making!
* When you're incrementing or decrementing, you want to spread out those stitches, otherwise the object will have a bulging or scrunching effect in that one spot.

I wondered if it was possible to express crochet patterns in a way that was more like SQL or CSS, than COBOL. Was it possible to declaratively express the desired outcome of a crochet pattern, that left room for creativity in the hands of the crocheter? I wasn't sure, because I hadn't really seen any declarative representations.

Then, I learned about freehand crocheting.

## Writing the program is the easy part

There exist people who can look at a finished object, and figure out how it's made without following a pattern. That, to me, felt like an amazingly difficult thing to do. I started searching online for advice about how one can get started with freehand crochet.

Generally that advice was:

* Start with patterns for the thing you want to make, and make lots of different variations of that object. You will eventually learn the themes that inform pattern design for that category of objects.
* Learn to modify existing patterns. Find a pattern that's _close_ to what you want to make, and figure out how to change it.
* Try lots of different crochet styles and stitches.
* Be patient with yourself. Try to focus less on correctly producing finished objects, and more on the process of learning and building mental models.

I realized that the skilled freehand crocheter isn't necessarily a natural genius. Rather, they just have more experience at implementing a diverse range of projects. All of those rules that I figured out earlier -- that's what freehand crocheters do, too! They just have spent a lot more time doing this, and learning many more rules than me.

And... that's when it clicked. This is also what senior engineers are. Because that same advice for freehand crocheting sounds a lot like programming advice that I got when I was early in my career:

* Start with a problem you want to solve, and come up with several different methods of solving that problem. You'll eventually learn a few common themes for solving this category of problem.
* Learn to read source code, and introduce tiny changes to an existing program.
* Try lots of different programming languages and paradigms.
* Be patient with yourself. When you're programming for self-education, focus less on having a polished outcome, and more on the process of building.

Senior engineers aren't inherently smarter or more talented than their more junior peers. They just have spent more hours thinking about different programming challenges, and they've encountered and solved more categories of problems.

## Closing thoughts

If I haven't convinced you yet that there are a ton of parallels between computer programming and fibre arts, here's one final observation:

Programmers. Who has ever bought a domain name for a side project that you never got around to? Or just started a ton of side projects... (show my abandoned GitHub projects)

I regret to inform you that crocheters and knitters are absolutely the same, but instead of buying domain names, we buy yarn. So. Much. Yarn. (show my shameful stash)

There is quite a lot that tech can learn from the crocheting and knitting community, and perhaps vice versa. Thanks for coming on this meandering journey with me, and I hope you'll look for computer programs in many more unexpected places!
