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

There’s a certain strangeness I feel around vibe coding. While a lot of creative practices can have boring, unenjoyable elements (I don’t know anyone who just wants to stretch canvas all day) we tend to make paintings because we love painting, not because we love having made paintings. The structure is reversed with vibe coding. I don’t vibe code because I love spamming requests to a large language model, I do it because I want to make interactive systems more quickly. While I don’t enjoy some aspects of coding, especially when problems are highly specified in a non-creative setting, I actually find it fun usually. 

I’m sure this rocky relationship with a new way of making has been true for makers throughout history as we automate the fun out of everything. I think it’s important to liberate ourselves a bit from what the corporate approach to coding to make the bare minimum finished product as quickly and cheaply as possible. What if we think of coding more like craft, like knitting or weaving? **Use vibe coding if you want to do something quickly, but also allow yourself to enjoy your craft.**


## My Recommended Methods:

Mess around with different models. They will continue to change. I found the best models I had access to were Gemini 2.5 pro and Claude 3.5 Sonnet. I probably would not pay for more tokens on better models since I hate paying for stuff but as a creative technologist it might be more worth it than paying for an Adobe product.

Arguably the most useful aspect of vibe coding is in the domain knowledge gathering stage. I wanted to make a piece of video jockeying software. I had no idea what libraries or frameworks were even available to do this. Asking questions like “how might I do xyz” and doing a lot of research early on into the different suggested methods is incredibly important. Google searching should also be used during this stage to actually check documentation but sometimes what you want to do is kind of strange and the models can propose some harder to find options more quickly.

After 250 lines of code, vibe coding projects start to get bloated and making edits that don't break everything gets harder. I would recommend chunking things into seperate files only give the model the structure of the working parts, much like how you might actually write good production code.

While I can honestly say I have been too lazy to do this on several occasions, double check that any libraries you are downloading are real and not slopsquatted. This doesn’t take too long and you might find some documentation that might be helpful to you later.

## You still need to know how to do some stuff

Even with all of the automation in vibe coding, you still need to know enough about real programming to know how to ask the right questions, debug, and most important ensure that your code is running efficiently. On several occasions when I was making the corpus conversation project especially, I had to actually read the code, understand what it was doing, and propose a more efficient thing to do. This is the main skill that you need.
I think anyone who wants to do large vibe coding projects should know how to code, even basically, and then have a basic mental model of the following:
- O(n)
- Parallelism and Concurrency
- Basic data structures (and especially the sense of how changing data structures can change the efficiency of certain tasks).
- How to structure your code and files

# Mini-Projects

### BibleGPT

I trained my own small GPT model on the Bible using Andrej Karpathy’s nanoGPT library: https://github.com/karpathy/nanoGPT. Less vibe coding here and more using Gemini to parse error messages, which was very useful. This project really helped me get fast at setting up environments and gave me a lot of confidence to do other things.

### Corpus Convos

For this project I was trying to see if I could construct conversations, scripts, or dialogues between corpora by placing similar sentences next to each other. First I tried using SpaCy but then moved to the more apt BERT for getting sentence similarity. Transformer models like BERT actually work really well for this. The most successful way I arranged the sentences was just by starting with one sentence, then finding a unique sentence most similar to that and repeating with subsequently chained sentences. I also tried appending the sentence to come after the most similar sentence but that did not yield good results.

This, like the previous project, was a good application for vibe coding since my domain knowledge of computationally quantifying semantic similarity was low going into this.

One thing I learned was to make sure I was really reading the code to make sure it was actually running efficiently. The slop code was initially running sequentially and re-calling a super heavy function over and over again that only needed to be called once. Thankfully prompting it to run in parallel and only call that function once did work.


### Video jockeying tool

I wanted to make a video jockeying tool for another class and very lazily vibe coded it. There was a glitch in the playback that was actually kind of interesting so I kept it. Overall the impression I had from debugging the program was that it was very unstable, but that instability was interesting to me.

![gif of video jockeying](/img/img1.gif)

### Talk To God

I was re-visiting my Bible project and made a program where you say something, it clones your voice and uses whisper to transcribe it, then reads that transcript using the voice clone. This was to be a proof of concept for a more conversational mode of engaging with my Bible model and by extension God. A lot of this worked honestly scarily well. However, the one shot voice cloning that I could access with my hardware locally just was not good enough to make a good facsimile of someone’s voice.

### Wizard Cippy Thing

This was really the point I went in the wrong direction. I liked this idea of a conversation with a janky machine and wanted to make an evil Wizard Clippy thing that lived on your computer, talked to you, and responded to your screen. I got optical character recognition to work off screenshots it took of the desktop screen, a local Gemma model running, and a basic GUI but the Gemma model just could not be evil enough for me and I sort of ran out of steam on the project. I found working with the GUI to be incredibly frustrating and realized that if I wanted to get the results I was looking for with the model, I’d have to probably train a new one myself which I did not have time to do.

### Sentence Similarity Visualizations

I revisited the corpus conversations. I tried a few more methods to get better conversations going then decided I needed to get a GUI up and running. Being in vibe coding brain I just was like “make a GUI for this” and it produced some really trash GUIs using some python libraries which I fought with for a few hours. Then I remembered that I'm decently competent with JS/HTML/CSS and figured I should lean into that. I got Flask up and running which was definitely the right choice and started making visualizations with D3.js. I fought with it more and ended up in the funny position where I realized I would actually be faster and less stumped doing actual programming instead of vibe coding. I have domain knowledge here, I can move swiftly. Another funny thing was that as I was working on the GUI, I also was trying to find a more efficient way to find nearest neighbors with high dimensional vectors so I could have larger networks of sentences. I looked up some efficient data structures for that, found ball trees, and was immediately able to implement them. After it builds these trees, it runs super fast.

The main point of frustration I found was that after about 250 lines of code, new edits continually break things and start adding inefficiencies. I think a better method would be to chunk all the code into separate files and only give the model the structure of the working parts, much like how you might actually write good production code.

