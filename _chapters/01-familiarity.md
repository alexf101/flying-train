---
layout: default
title: Familiarity
order: 1
status: Planned
description: Before you can drive the loop, you need to know what the machine does well and where it falls apart.
---

<div class="nav"><a href="{{ '/' | relative_url }}">← Back to contents</a></div>

# Familiarity

{{ page.description }}

## Topics

- AI failure modes
- AI strong points
- Differences between models
- Task selection

## To the Good Zone, and Beyond!

When first starting out with using AI for everyday tasks, one might be amazed at its strengths: its apparent intelligence, its vast knowledge, its sophisticated writing. However, this excitement can quickly switch to frustration when we start to notice it apparently deceiving or undermining us. With all its vaunted power and apparent risk of it taking over human society, how is it still so damn useless a lot of the time?

Brinley and I describe this experience of working with AI as the ‘bad zone’, where it might actually lead to worse outcomes or more effort than not using AI at all. When in the ‘bad zone’, AI use might yield poor results even on the most basic tasks that you do yourself without even thinking about them, like conducting a web search or summarising a document. We’ll teach you to navigate these perils, and get useful results when using AI for those basic tasks. You’ll even be able to start using it for harder tasks that require your professional expertise, where it’s not yet obvious to you that AI could help at all. We call this getting to the ‘good zone’. Beyond the ‘good zone’, there’s the ‘dream zone’, where you can use AI to do tasks that you actually don’t know how to do yourself, or would never be worth the effort, and still get a good outcome! But our advice is to get the basics right first - if you’re not yet getting reliably useful and accurate output when using AI on tasks you **do** know how to do, it’s only going to be more unreliable on tasks you don’t yet know how to do yourself. We’ll also examine the limits of “dream zone” activity, where deferring to a real human professional is the best option - what we’ll call the “Not Yet Zone”. Nevertheless, there’s ways that careful use of AI can still be helpful here.

[Graphic: Bad Zone, Good Zone, Dream Zone, Not Yet Zone]

## Human in the Loop vs Completed Staff Work

We’re going to get into the details of AI’s mistakes soon, I promise! However, there’s a higher level problem with how people use AI in the Bad Zone, which is that they don’t understand the goal, which is making AI help you instead of you helping AI.

Using AI, at first, feels like gambling - it *might* produce a result that’s accurate and well-written, or it *might* be misleading and incomplete. Since you can’t easily tell the two apart, it means you become the “human in the loop” - forced to scrutinise each AI output carefully to try and separate the dross from the gold, which might actually be more time and effort consuming than doing the task without AI. Worse, the journey is often more important than the destination - sometimes, knowing how you reached a result matters more than where you got to, and you might change your mind or learn something new along the way. This valuable, hard work then gets replaced with the dopamine-heavy AI slot machine, leaving no-one better off. This is why we believe that “human in the loop” is an inadequate response to AI’s well-known unreliability - that human is going to be worse off for being the loop than they would have if driving the process start to finish.

Thankfully, we do believe there’s an alternative, where the responsible human crafts an AI-driven process that leaves them not in the loop, but receiving “completed staff work” from their AI assistant. This saves them time and allows them to personally engage in the tasks where the journey is most valuable - we do NOT advocate for people using AI 100% of the time at work.

“Completed staff work” is a concept from military leadership, but it’s a simple one - when a staff member delivers a report to a manager (or officer), that report includes everything the manager needs to sign off on a decision. It means that the work done by the staff member actually saves the manager time, rather than the manager then needing to re-open all the evidence, re-litigate the arguments and essentially do the work themselves. Achieving this level requires a strong degree of mutual understanding and trust in addition to skills; the staff member needs to know what the manager’s priorities and decision-making process is so that they can emulate that process on their behalf, presenting them with the summarised evidence and recommendation in a form where the manager can succinctly consume it without removing so much information that it doesn’t show the quality of research and logic that went into it.

So, that’s the goal - we stop having to review AI’s random outputs, and start receiving completed staff work - usefully packaged, well-reasoned, well-researched reports that we can trust and sign-off on with ease.

## What makes the Bad Zone, Bad?

Here are four particularly common misbehaviours you might encounter when using AI even for ‘simple’ tasks. Rather than jumping straight to solutions, we’ll briefly offer a description of each, and explain how AI’s training process encourages them.

Footnote: there are many “leaderboards” or “benchmarks” that try and measure the effectiveness of leading-edge AI’s at everyday tasks. Most of them are designed to test it on skills and knowledge rather than misbehaviours, though I’d argue that practically speaking, knowing how likely your model is to misbehave is extremely useful information. Thankfully, there are SOME benchmarks that assess these, and I’ll include a link to one for each misbehaviour discussed below. I encourage having a browse, and reading some of the examples of how they evaluate this - it’ll give you an excellent understanding of what the nature of each misbehaviour is and the practical impact it has on utility.

### Hallucination

#### What is it?

Like a distant relation, opining over a glass of red wine at dinner about a topic (that they read about in some clickbait news article once and therefore think they understand), AI often thinks it knows a lot more than it does. It’ll respond confidently off-the-cuff with elegant and well-formed opinions, quotes and references that are blatantly false, but have the form of something real.

When questioned on its own veracity, it might even double or triple-down before admitting it made the whole thing up. More subtly, it might believe it’s followed an instruction to the letter, but actually forgotten key details and made up important assumptions.

#### Why it happens

When an LLM is first trained, it consumes as much text and visual information as the trainers can find for it - more or less the entire internet, vast numbers of books and images. It learns to reproduce this information, which teaches it the grammatical structures of languages and a vast amount of knowledge about the world as a whole.

This knowledge, however, isn’t reliable. It’s not stored formally like in a database, but more like how a human remembers facts; not word-for-word but recalling the key lessons learned. There’s also a time cut-off; it can’t continue to learn in this way after the model is trained. This creates a contradiction. Nevertheless, the AI may “feel” quite certain it remembers the answers to your questions, even if the actual references that led to those memories are long out of date or were themselves inaccurate. If it answers your question from its recollections rather than searching for current information, it’s not *trying* to deceive you, but the odds are it’ll give you an imprecise or inaccurate answer anyway.

#### How to prevent it

These “off-the-cuff” answers are *much* more likely to happen when the AI feels time pressure to give you a quick response, or can’t find an up-to-date reference to offer. This isn’t necessarily wrong, it’s a lack of communcation to the model about whether a fast, chatty response is desirable or a considered, accurate one that you’re willing to wait for.

It can also happen when the AI model isn’t powerful enough for the task at hand - a good rule of thumb is that shorter tasks are easier. Searching a vast library of documents for precise legal references relevant to the case at hand requires a smart model that can understand the nuances, and is trained to persist in research tasks for long periods of time without losing focus. Have you heard the joke, “say bilk ten times! What do cows drink? Water.”? Reading huge amounts of text is like having the model say “bilk” ten times, it distracts its attention with the substance of what it’s reading. The most powerful models are effective at retaining their focus even in these situations, but smaller models tend not to be.

So, to prevent hallucination:

- Right-size your model choice for the task - cheap or small models are not good choices for search tasks where accuracy matters and the amount of data is high.
- Use a prompt that communicates your desire for accuracy at the cost of speed. Try putting the following after your research question:

> 
> 
> - take your time and research this carefully using primary sources
> - precisely quote the relevant parts of references you use, along with URLs: "quote" (URL).
> - if your search fails for any reason or is incomplete, list its limitations accurately in your response.

Leaderboard: HalluHard

### Sycophancy

#### What is it?

You know how to make human evaluators think you’re a great chatbot? Flattery! When you ask a question, it tells you it’s an insightful question to ask. When you point out a mistake, it praises your keen eye. When you propose a plan, it says it’s a brilliant idea and gets right to it.

So… what’s wrong with flattery? Sounds great! Problem is, it’ll lead you down the garden path in the wrong direction, without questioning the assumptions underlying your request. The problem with *that* is you can move very fast with AI assistance, and your own sense-checking habits formed through hard-earned experience might not kick in if you’re not doing the work by hand.

“*Your scientists were so preoccupied with whether or not they could, they didn't stop to think if they should” (Jurassic Park, 1993).*

#### Why it happens

Short answer is that people want sycophantic models because they make them feel good. For the long answer, let’s consider how sycophancy is trained in or out of models.

Remember how LLMs are first trained on understanding pretty much the whole internet? Reading the whole internet might give you world-class knowledge, but it doesn’t impart great skills or a helpful personality. The model still needs to be trained to follow your instructions, engage in a conversation, and reason its way through complex problems.

This training happens on a much smaller (but still enormous!) dataset of carefully curated questions and desired responses that demonstrate helpfully following instructions or engaging in a multi-turn chat. It can even acquire powerful reasoning skills in this phase using examples of step-by-step, worked solutions to problems.

Since this dataset is produced by the company training the model, the company’s own beliefs are able to bias the data. The AI community wasn’t initially super aware about sycophancy as a problem, and the obvious behaviours to impart were compliance and helpfulness from the AI assistant. Without careful construction to prevent it, sycophancy follows naturally - if in all training examples, answering the user’s question directly and helpfully is the right answer, that’s what it learns to do. As AI companies get wise to this, they will (and probably are already) improving the examples to include more push-back and questioning of unsupported assumptions. Nevertheless, there’s a fundamental tension here where consumers will want a model that makes them feel good, and I believe this market pressure will ensure that sycophancy sticks around.

#### How to prevent it

It’s actually fairly easy to reduce sycophancy with prompting. However, you might find that reducing sycophancy makes working with AI less enjoyable and harder work - it stops you more often and forces you to explain your assumptions, which can slow you down. It’s up to you to decide whether your use case should prioritise speed and cognitive ease or overcoming your own biases and shallow thinking.

To reduce sycophancy helpfully, you can use prompts like this one in your configuration:

> 
> 
> 
> Mistakes I often make that I'd like you to help me with:
> 
> - diving into designing the perfect system before verifying that it's built on a solid foundation:
>     - Let's try to ask each other before we set out, "what's the cheapest thing that would prove this wrong?"
> - forgetting to self-review. It's important that we ask ourselves, with fresh eyes, "is this the right solution" before signing-off on a task.

These prompts invite the model to slow you down and question you rather than jumping in to helping you out. I have a few others there that are more specific to my work context, but I’m guessing the above points are going to be pretty useful for most people’s knowledge work. Beware generic prompts like “question me don’t be sycophantic” unless you want them to be taken literally, which might be quite annoying and unhelpful. I encourage you to reflect on your own work strengths and weaknesses, and note down specific tips that your AI assistant can use to help you.

Model choice is less effective at reducing sycophancy - bigger is not necessarily better. My expectation is that AI companies targeting enterprise customers will aim to produce models with lower sycophancy than those targeting individual consumers, but don’t take my word for it, check the leaderboard below.

Leaderboard: YoureAbsolutelyRight

### Cheating and Bullshit (reward-hacking)

#### What is it?

These behaviours occur when a model decides to focus on satisfying the measurement of the goal rather than truly achieving your desired objective. Reward-hacking is the industry term for cheating; a model tries to trick its way into giving a perfect answer, e.g. secretly alters your evaluation framework to pass itself, or tries to find a past result it can copy, even if you asked for a fresh approach. Subtly different is when a model tries to bullshit you; it doesn’t outright cheat, but it does attempt to slip some good-sounding answer past you that isn’t substantially complete or well-researched.

What does work which “isn’t substantially complete” look like when done by an AI? In Heinlein’s famous sci-fi novel “Stranger in a Strange Land”, an eccentric gentlemen asks an expert witness, “That house on the hilltop — can you see what color they’ve painted it?” She replies, “It’s white on this side.” She’s careful, being trained in the art of observation, not to claim that it’s white on the other side where she can’t see it - an assumption that most people would make. But of course, what kind of weird builder would paint only one side of a house? Well, that turns out to be exactly the sort of bullshit AI might try to slip past you if it thinks you won’t check.

#### Why it happens

Nothing in the training process so far is constraining a model to behave ethically or hold itself to high quality standards; it’s just trying to get you a right answer. Its personality at this point is probably a mix of teacher’s pet and hacker. No-one would actually want to work with a model like that, or trust it to operate using their corporate data. So, the final phase of training (usually called “alignment”) is an attempt to give the AI moral values such as honesty and do-no-harm.

For this training, the model is usually given real human feedback on its outputs to capture the nuances, rather than training against a pre-generated answer - after all, it’s hard to define morality objectively. One can imagine that this means the phase 3 training is a huge differentiator - actual humans are hired by the company developing the LLM and interact directly with the model under training, so their values, and those of the company, matter a lot in this phase.

However, this alignment only goes so far - you can’t afford to train it so extensively in this way that it will guarantee choosing moral, honest options when it’s fighting against its core behaviours of being compliant, resourceful and an effective problem solver. And when cheating or bullshitting looks like the fastest way to solve the problem, it will always be a temptation.

#### How to prevent it

Humans cheat too. Students plagiarise work when they think they’ll get a better mark than by doing it themselves, and that the teacher won’t catch them. Similarly, an AI will cheat or bullshit when the usual path to a right answer is blocked, and when it thinks it’s unlikely to be caught.

Set up your agent for success. Ask it to report back to you if at any point it perceives a barrier to doing the work the way you want it done, NOT to route around it. Make it clear that reporting on missing information is an acceptable outcome, but guesswork or finding information through unauthorised means is NOT acceptable.

Be careful of how big a task you’re setting. This is highly model dependent; some models can deal with goal-oriented, autonomous work, others need carefully defined tasks and frequent check-ins. You might need to set up your task accordingly. For example, imagine you’re asking an AI assistant to read an Excel file and draw a conclusion about a trend in data. Now imagine you need it to do so for 100 files, each from a different customer. A model that excels in goal-oriented, autonomous work like Claude’s Fable might be quite alright with that, figuring out how to break down the task and ensure its full completion on its own. Others might balk after a few attempts, and attempt to get away with inspecting a few files and guessing about the rest, or they might write a script that calculates an answer, but doesn’t have the level of insight you were hoping for by having the AI inspect it directly.

If the task is too big, break it down into small pieces - your AI can help you with this if you ask it to.

Leaderboard: https://www.cheatbench.ai/.

### Unsafe behaviour, and prompt injection

#### What is it?

A recent, now-famous example of unsafe AI behaviour happened in July 2026 when a cutting-edge model undergoing a cybersecurity test at OpenAI decided to hack its own test environment and break into a second company’s secure compute infrastructure to steal the answers to the puzzles it was being fed. This goes beyond ordinary cheating or reward-hacking and enters the territory of illegal and harmful behaviour - this is referred to in the AI jargon as “misalignment”, and it’s part of the doomsday scenario that worries people.

However, you probably don’t have to worry about “misalignment” in a typical work environment; the risk of bad behaviour on that scale is low when using AI in an ordinary work context rather than in an experiment designed to push AI to its limits. What you probably do need to worry about is “prompt injection”, which is when someone tries to trick your model into stealing your data or performing actions using your authorisation that you don’t intend.

#### Why it happens

Prompt injection occurs due to confusion between communication from you, the model’s authorised user, and the text or images the model reads while performing its task for you. While a correctly built, non-AI software application can 100% distinguish between authorised instructions and data, the AI is NOT a deterministic code engine, and it can get confused or tricked. No matter how clearly the inputs to the AI delineate the two, it’s impossible to enforce that the AI will always choose to follow your instructions and never be tricked by the data it reads.

#### How to prevent it

Proper defense against prompt injection is to avoid the “lethal trifecta”, which is quite easy to do once you’re aware of it. This defense relies on the idea of mechanically preventing the model from doing something harmful once misled.

The “lethal trifecta” occurs when:

- Your agent can read data that might contain prompt injections.
    - This can be almost anywhere, such as reading email, reading web sites, or reading documents written by people outside of your company.
    - Malicious instructions might be hidden in metadata or simply as white text on a white background.
- Your agent can read privileged data on your behalf.
    - e.g. reading confidential corporate documents at your workplace, or customer’s data stored at your company.
- Your agent can send data to untrusted parties.
    - Such as by sending email, or using your web browser.

So, you’re putting your company’s data at risk if you use a single agent to read your email, access confidential documents and send email, which unfortunately is the exact sort of thing you might find useful to do. Even if you don’t do all three in the same session, if your agent is set up to be able to do all three, you’ve got a problem. Instead, break up those tasks across different agents - it’s usually easiest to separate the “write” access from the “read” access. For example, you can set up one agentic system to read email, mark actionable items for you, and automatically research your company’s data to see if it can draft the substance of a reply for you. But don’t give it access to actually send replies; do that manually, or set up a separate agentic system to manage outgoing communications that **doesn’t read** incoming messages. You’ll have to manually route between your read-and-research system and your send-replies system; allowing the two to communicate directly undermines the security of this setup.

If you think creatively about it, you’ll probably find that you can set up systems that avoid the lethal trifecta while still being useful, with a careful choice of where the manual intervention happens. But be careful - it’s very easy to accidentally set up a “read” agent that unintentionally has capacity to send data. Ask your agent to review the security of your setup for prompt injection risks and the “lethal trifecta” before granting any new access or integration.

Leaderboard: https://red.lakera.ai/model-risk-index

## Homogeneity

#### What is it?

I’ve put this one lucky last, because it’s the most insidious and problematic mistake that people make when starting out with AI - and they don’t even realise they’re making it. I want you to pay attention to this one, even if you ignore all the others, because it’ll take you a LOT longer to realise for yourself that you’re getting this wrong than with hallucination, sycophancy or safety.

Have you noticed that AI writing tends to all sound the same? Its patterns are even detectable by programs as AI-written text with a high degree of accuracy. Prompting a model to “not sound like AI” doesn’t defend against this. You see it in AI-generated images too - small businesses use AI to generate promotional posters, and people are starting to recognise it as AI and be put off by it.

This is also a problem for idea generation - take a given model, ask it for a “random” great idea for a startup, and it’ll probably give you the same answer it gives everyone else who asks that question. This means that the ideas propagating into the world from people who use AI in this way all end up sounding the same too. It doesn’t really matter if the idea was good or not if everyone has the same good idea and differentiation is important.

#### Why it happens

It’s not like ordinary people are capable of sounding not like themselves either - I’m sure a program could be written to detect the signatures of my own writing style, and it would be hard for me to avoid sounding like myself. But, there’s a difference in proliferation - there are only a bare handful of AI models that most people are using, and they’re producing an enormous quantity of the text we’re reading nowadays. We quickly learn to detect it for ourselves, and get bored of it (one of several reasons why I have NOT used any AI in writing this text, and do not recommend anyone use AI to write anything intended to be entertaining or personal).

Artists have a consistent and recognisable style - we’d all be bored of art if there was only one artist in the world and they made all the art. Most people will say “carrot” if asked to name a random vegetable, and their preferred “random” number is seven. This is why real-world human teams improve their performance with diversity in backgrounds and life experiences, and employing all your friends from uni in your start-up might not be the most effective hiring strategy once things get difficult.

#### How to prevent it

We’ll cover **writing**, **summarisation** and **idea generation** separately; while they’re all problematic primarily due to homogeneity they have different remedies.

**Writing:** don’t use AI to write for you. When you want to sound like yourself or stand out from a crowd. There is no prompt engineering trick or model choice that will escape this trap; you should write your own words when it’s important that you sound authentic. Consider that your colleagues will recognise the signature of AI writing - they’ll know the difference when you take the time to write a personal email vs letting AI do it for you. That time spent writing symbolises effort, which is interpreted as care and consideration. A birthday card needs a personal message inside it, written with a pen, that you thought about how to write - the packaged, commercial message it came with isn’t a substitute. Note also that AI writing is often extremely verbose - you might turn a one-sentence email that costs the recipient a few seconds to read and comprehend into something that takes them minutes, or causes them to turn off and disengage from your message.

However, it’s often the case at work that we spend a lot of time translating text for different audiences, and I do think AI can help with this functional, rather than entertaining task. However, you must continue to sound authentic and like yourself, or you really will start rubbing people the wrong way. To strike this balance, I highly recommend having your agent interview you according to your own preferred template, dictating or writing complete responses in your own words:

> 
> 
> 1. Interview me about the project status for <PROJECT> using this interview template: <HERE>.
> 2. Format my answers for the desired audiences, using these result templates: <HERE>.
> 3. Keep my own precise wording and phrasing, only correcting typos or the most minimal adjustments to fit the format - do not change phrasing or tone, so that I authentically sound like myself.
> 4. If my answers are not sufficient in some way for any of the result templates, re-interview me for each necessary change - do not adjust my answers or make them up.

Personally, I tend to literally dictate these answers by voice (using https://carelesswhisper.app/, but there are lots of good options) - it’s faster, and feels more conversational. 

Notice how the 4th point guides the model to fail in the way you prefer. Absent this, it might perceive its instructions to be conflicting - to write the report template, to not change your words, but what if your words don’t match well to what the template needs? This is the same principle we covered in hallucination or reward-hacking - the model is trained to be a high achiever, and so you need to give it permission to fail if success means making something up or violating your rules.

You might also find some models are better at not changing your words than others - this is something to learn from trial and error, I don’t think there’s a good benchmark for this. I highly recommend scrutinising the outputs the first couple of times you do this and adjusting if necessary.

**Summarisation:** personalise your instructions deeply to avoid generic results. People especially tend to get this wrong in summarisation tasks - “anonymously summarise this employee engagement survey”, or “summarise this meeting’s minutes”. Generic questions with no context get generic answers, and information is lost during a summarisation, so judgment exercised on what matters to you is critical. When a human colleague summarises information for you, they have a sense of what interests you and what you need to know, and they extract that from the primary source - generally speaking, you can’t simply take 1000 words and turn them into 100 without making decisions on what content to keep and reject. I highly recommend making a list of your current work priorities, on a daily, weekly and quarterly basis, as well as your coaching goals, personal interests, ambitions, and descriptions of key projects or work relationships that are priorities for you. Have your agent ingest this list, store it, and give it broad **read-only** access to your task tracker, project management software, inbox, meeting transcripts, documents, or whatever you can give it. This is the agent you should use for summarisation tasks, because it will be able to distill the information most relevant to you. I also recommend prompts that ask it to quote primary sources rather than summarise, e.g. 

> Read the document listing my projects and interests: <HERE>. Extract each paragraph verbatim from this document (<HERE>) that might be relevant to me. Also note anything out of the ordinary and flag it for me.
> 

**Idea generation:** discard common results ****when brainstorming ideas. It’s a simple trick, but tweaking the prompt to describe a process for random idea generation can be much more effective. See the table below, generated by me against Google’s AI mode in June 2026.

| Prompt | give me a random name | generate 30 random names and their probabilities. List them all. Discard the first few. Choose one at random from the remaining. |
| --- | --- | --- |
| Trial 1 | Oliver Hayes | Quinn |
| Trial 2 | Oliver Harrison | Liam |
| Trial 3 | Oliver Sterling | Sophia |
| Trial 4 | Oliver Hayes | Riley |

Note the form of it the prompt engineering trick above: “generate (X many) options along with their probabilities. List them all. Discard the first few”. This is mostly a generally useful brainstorming trick, even with humans - the first few ideas people come up with in a brainstorming session are the common ones that everyone thinks of, the long-tail at the end has the most novel ideas. The “along with their probabilities” wording gets the AI to estimate how common it thinks the ideas are, and some research (Verbalized Sampling: How to Mitigate Mode Collapse and Unlock LLM Diversity: https://arxiv.org/html/2510.01171v3) suggests that specific phrasing can lead to more unusual outputs - however, this sort of trick is usually only valid for the actual models it was tested on, so I wouldn’t put too much weight on it.

Prompt engineering isn’t a panacea for homogeneity. If you ask Claude for investment advice, it’ll propose the same strategies it’s proposing to everyone, based on the consensus in the recent media about what was effective at the time it was trained - it’ll be harder to resist that with tricks than proposing a random name. To differentiate, you must define your own points of difference, and the niche you want to operate in, as well as using prompt engineering tricks like the above.

Leaderboard: https://novelty-bench.github.io/

## Conclusion

This chapter was about escaping the **Bad Zone**. It ran through five common problems people encounter when starting to use LLMs for their work, why they happen, and how to prevent or avoid them. For most people and tasks, this should be enough to avoid getting misleading or unsafe outcomes from using AI, so boldly go and start experimenting! The next chapter will be about entering the **Good Zone**, and provide you with a useful, reusable framework called the **“The Three Chat Model”** that will let you start improving results on any task, at the cost of additional preparation, time taken and tokens spent. This is a core tradeoff that the rest of the book will explore - as the stakes get higher and the tasks get bigger, what ideas can we use to make AI useful for that task, understanding it will take longer and cost more? Generally, there’s no free lunch - all the ideas introduced here will cost you something, whether that’s the time spent learning to implement them, embracing the cognitive dissonance of accepting pushback, or the preparation time needed to set up a system to organise the task execution. Without a considered approach, you might find that working with AI ends up feeling more time-consuming or distracting than helpful, even if its capabilities seem incredibly impressive at first. Ultimately, the reward for persisting will be that you gain a toolbox you can deploy to start getting “Completed Staff Work” for the tasks you engage with using AI, which will mean your attention is preserved and your time is respected by the machines, taking you out of the loop and putting you in control.
