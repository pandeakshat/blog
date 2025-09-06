---
title: Mistakes of a Programmer
description: Mistakes of a Programmer
pubDate: 2023-10-18
heroImage: "1-mistakes-of-a-programmer.webp"
readingTime: 5 min read
tags:
  - programming
  - mistakes
  - experience
  - growth
---

  Disclaimer: I am no professional, or even at the end of the road of learning, as my steps tread through the code, to become a programmer I’ll feel content with.

Programming at times, is accompanied by frustration, when the errors pile up, and you’re stuck with the simplest missing “;” or even the scope not resolved for objects leading to errors that don’t point out exactly at the mistake, or even a missing indent that makes you go through each line to find the issue you missed out by ****mistake****.

Errors, and mistakes, are part of a programmer’s life, and we live with it till the day, we code.

The only viability of mistakes in coding is, if we learn to identify them, we can make habits to avoid them, and hence, I compiled a list through scourging online, and my own experiences to plot a list, of the most common mistakes, and how to avoid them.

It all starts with, understanding the flow of coding, any program, any project, any time. As it goes :

Think => Research => Plan => Code => Validate => Modify.

Pertaining to the flow of coding, its obvious, the first mistake, lack of planning. Planning something, gives you a mental mind-map on how the process would go about, how the steps would be done, and how the structure will come to life. Coding is communicating your thoughts to the machine, to make it do what you desire, and as just randomly spouting your desires would not get you there, randomly throwing segments of code at a machine won’t work properly either. Programming is logic-based creativity, and it requires nurturing to not just make it work, but to make it work flawlessly. Planning is the necessary step, before coding. Yet, the catch is, don’t get stuck on planning everything before starting. I personally, have known people, who get stuck in an infinite loop of planning, refining the mental mind map to perfection till they reach it, before even attempting at anything. The key is, to understand the process and steps through the mind map. There is no perfect plan, and there will always be obstacles you will have to get through, that’s why, Plan to understand, not perfection. A perfect plan is unrealistic as it is immutable to changes, while the reality requires change and adaptations at every corner, be agile.

Let’s come to the coding part, if your logic is correct, and your syntax is on point with your logic, code will work, but, have you ever tried to look at your own code, or someone else’s code and been like.. wait? where is what? and you keep searching your way to find what logic is happening here and how is it connected to everything. Yes, that’s where we forsake the quality of the code, cause well it works! but that’s a bad practice. Imagine writing a letter with no spacing and divided parts, feels like a gibberish paragraph, even though it conveys your thoughts, even in proper tone, the lack of structure ruins it. Capitalization and indentation are important in coding, to make sense of it for everyone else who reads it. A few practices that go a long with, to ensure quality of a code is, ensuring a limit of 80 characters per line of code, and to divide logical segments of the code into functions ( always a good practice ), naming of variable should be kept as non-ambiguous as possible, gone are the days of having all variables as x,y,z or a,b,c and extras as p,q,r, assigning constants to keep it all stable and understand, shorter code is better, but only if it doesn’t forsake readability!

One more thing that we do, while coding is accepting the first solution, to hit the jackpot on the first try. There is none. Coding is an art-form which requires continuous improvements, better logic and improvised quality and flow between segments. Never be satisfied with the first solution ( unless you are on a deadline and submission is in a few minutes ). The first solution is right, no doubt, but to evolve and grow, its always better to improve on existing solutions to realize more solutions, better ways to get the solution, to simplify it, to reduce its complexity and increase readability, with quicker execution, less space consumption and so on and so forth. Moreover, in the off chance, your first logical solution to the problem doesn’t fit or work.. don’t be stubborn! quit. Coding is not about just having a solution, its understanding there can be many, to get through that mindset, think coding as a practice where the more you fail, and the often you fail, the more you will learn. Its important to be fluid in concepts regarding coding and your motives, its okay to be stuck, but its bad to be stuck and just keep at it, without just letting it go and looking at another way to get through.

Its also important to research about your code, google it! there is nothing bad in searching online, most codes and programs can be found online. We have all made our fair share of copy-paste for assignments or lab time, and researching is an important factor for the flow of code, you may never know what you were missing out, and someone on the internet has painstakingly shared all his thoughts for you to dive and collaborate with. Research, but don’t copy-paste, as its a learning process and if the only thing you understand is the problem statement, and copy-pasted, compared the output if it looks like its supposed to, then in all essence that’s been a waste of everyone’s time. if you are running out of time, and if you find exact solution, copy-pasting is fine, but only if you understand the code too. Give it a read, understand the logic, see what’s missing compared to what you thought, what is added that you never thought of, is there something different than how you would have done it, brainstorm it and then copy-paste and run. Stealing someone’s work and making it your own is plagiarism, but if you can take someone’s code and improve on it for your own work and make sure to attribute them, that’s the entire psychology behind open-source and collaborative programming.

As mentioned before, to maintain quality, all logical segments should get their own functions, this is the concept of encapsulation, and its beauty isn’t in the quality of the product or code that you wrote, its more in the maintenance of it. Ever tried to go back to something you coded a long time ago, scourging for the logical segments and getting lost in the scope of loops and variables? Probably. This is where encapsulation plays a role, if you encapsulate your code, where all logical segments get their own segment away from the “main” function, the easier it is to get back to, to tweak, modify, or reduce, whatever may be your motive. It reduces cascading effects when working on the code again, and its generally a good practice to keep high cohesion and low coupling between the code.

A key part to understanding and improving quality, and encapsulation is, understanding data structures and algorithm, to understand the limits and advantages of them, their uses in different scenarios and experimenting to find the one that works best. Not all algorithms and data structures are made alike, they have their own advantages and limitations, its important to know what works where, to dive into the depth of them.

Its also important not to reduce the quality of the code, while working on it, changes are necessary sometimes, but keep it clean! try to avoid duplicating of code just because it will increase the line of codes or cause somehow it works out, apply abstraction and make it look good. If something is re-used and employed multiple times, a function or a variable, some value or logic, specify a config file inside your code and just refer to that, to avoid causing issues with it and making it all worse. Its also better to avoid unnecessary conditional statements just to make things work, and temporary variables that have negligible use. Strive for cleaner code!

Readability is important if you are getting back to a code, and one way to make sure of it is to add comments for the things that don’t make sense, or aren’t obvious. Read that again. comments are for things that don’t make sense, or aren’t obvious. Comments are used to explain the Why of code, why this logic, why this data structure, why this segment and not What of code, like variable declaration and print statements that already include its use.

While comments are important, for better code, its also a good habit to conduct tests on it, to understand edge-cases and exceptions, and just if the code can work in most scenarios. not everything can be “its not a bug, its a feature” mentality. Testing-driven-development is always more stable than just coding and testing it once, to look for errors. As, sometimes, some inputs may just work with your logic, that doesn’t mean your code is right generally, its just right for the particular input, and for some other inputs, it can go wrong and you will embarrass yourself, so why not test it automatically with random inputs to avoid such a scenario.

Document your code if necessary, with exceptions and edge-cases, with comments and encapsulation and abstraction. Undocumented code is prone to errors and can lead to a longer process during debugging.

As you are not the only one that would be employing that code, it could be your friends or teacher or clients and colleagues that may use that code, its a good practice to understand and look through the end-user experience. Test the code as if you are in their shoes, look from their perspective to understand if it makes sense, and can they work with it, all people have stupid friends, if you dont.. you are.

The final few segments of mistakes, that are general or have been personally committed by yours truly is about the aftermath of codes.

Let people look at your code, and well let them criticize, accept them, see what they are looking at, that you don’t see, and improve, the one who doesnt dare to change and evolve, can become very stiff and useless, given that coding is a forever-learning process, the day you stop trying to improve is the day you slowly start dying.

One more thing, I particularly had trouble with, is understanding the tools necessary, the IDE, the pre-requisites, and so on. It is a part of research, understand what you need, and what works for you, and always look for better, even if its a bit complex, learn the new. As long as it streamlines the processes of your future and improves your efficiency and work quality.

Learn git, its awesome, and the more you learn, the easier your life becomes to collaborate and share. Seriously.

Finally, the mistakes everyone has gone through, errors. Errors are the wounds you get, without them, you cant really say that you are trying hard enough to improve, mistakes are a part of life, errors are a part of code. Make errors, see them, understand them, operate on them, remove them. The more errors you make, means more are you trying to work and improve, and the more errors you solve, the better you get.

Take breaks, refresh, make errors, correct errors. Code!
