# Vibe coding for creative practice
I spent the past two months working on six creative coding projects, extensively using vibe coding. This was an exploration in vibe coding for creative practice and helped me test the waters of what I could achieve for a variety of projects in different domains.
 
I am an alright programmer. I can make an interactive website pretty easily, write C++ for Arduino no problem, and I have a decent grasp of basic data structures, parallelism, and concurrency. I’m not fabulous however. I still definitely have some large gaps in advanced mathematics, data structures, and algorithms which allow for highly efficient specialized systems as well as domain knowledge for different languages (for some reason I never really learned Python).
The projects I tackled during this period were ones that would have probably taken me the whole two months each and I was able to get something down for them within a few days by vibe coding. While there are many things vibe coding is not good for, overall it can really speed up the process.

## What vibe coding is great for

Vibe coding is great when you don’t know what you’re doing. I didn’t have domain knowledge on basically all the projects I worked on except for the sentence similarity visualizations. Vibe coding helped me get things working quickly in domains I was not familiar with. It is also surprisingly good at implementing complicated data structures and algorithms that most people (myself included) don’t understand. When I was working on sentence similarity visualizations, I wanted a faster way to find similar sentences, especially since I wanted a really scalable system that could handle upwards of 100,000 sentences. I know that ball trees do something with hyperspheres to allow for really fast nearest neighbor searches of multidimensional vectors but how they work is beyond me. However, Gemini was able to get ball trees working super quickly.  

## What vibe coding is not so great for

Vibe coding generally fails when making GUIs. You can definitely vibe code a GUI but it will more often than not look pretty bad. There’s something very funny about the fact that these models can solve very complex problems while also failing to do one of the simpler programming tasks.
Vibe coding also generally fails to make well structured code. It will put all CSS and Javascript into your index.html. For reference, this is not good.

## The labor is no longer fun

There’s a certain strangeness I feel around vibe coding. While a lot of creative practices can have boring, unenjoyable elements (I don’t know anyone who just wants to stretch canvas all day) we tend to make paintings because we love painting, not because we love having made paintings. The structure is reversed with vibe coding. I don’t vibe code because I love spamming requests to a large language model, I do it because I want to make interactive systems more quickly. While I don’t enjoy some aspects of coding, especially when problems are highly specified in a non-creative setting, I actually find it fun usually. I’m sure this feeling has been true for many people throughout history as we automate the fun out of everything.
I think it’s important to liberate ourselves a bit from what the corporate approach to coding: make the bare minimum finished product as quickly and cheaply as possible. But what if we think of coding more like craft, like knitting or weaving? Use vibe coding if you want to do something quickly, but also allow yourself to enjoy your craft.


## My Recommended Methods:

Mess around with different models. They will continue to change. I found the best models I had access to were Gemini 2.5 pro and Claude 3.5 Sonnet. I probably would not pay for more tokens on better models since I hate paying for stuff but as a creative technologist it might be more worth it than paying for an Adobe product.

Arguably the most useful aspects of vibe coding is the domain knowledge gathering stage. I wanted to make a piece of video jockeying software. I had no idea what libraries or frameworks were even available to do this. Asking questions like “how might I do xyz” and doing a lot of research early on into the different suggested methods is incredibly important. Google searching should also be used during this stage to actually check documentation but sometimes what you want to do is kind of strange and the models can propose some harder to find options more quickly.

While I can honestly say I have been too lazy to do this on several occasions, double check that any libraries you are downloading are real and not slopsquatted. This doesn’t take too long and you might find some documentation that might be helpful to you later.

## You still need to know how to do some stuff

Even with all of the automation in vibe coding, you still need to know enough about real programming to know how to ask the right questions, debug, and most important ensure that your code is running efficiently. On several occasions when I was making the corpus conversation project especially, I had to actually read the code, understand what it was doing, and propose a more efficient thing to do. This is the main skill that you need.
I think anyone who wants to do large vibe coding projects should know how to code, even basically, and then have a basic mental model of the following:
- O(n)
- Parallelism and Concurrency
- Basic data structures (and especially the sense of how changing data structures can change the efficiency of certain tasks).
- How to structure your code and files


