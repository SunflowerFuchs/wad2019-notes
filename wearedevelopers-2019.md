# WeAreDevelopers conference 2019 in Berlin

---

## Thursday

### Congress opening talk

what a fucking opening, now i'm definitely awake

to participate: slido.com #wad2019

### Where Machine Intelligence Ends and Human Creativity Begins

TODO: look up if xkcd re: AI in board games is still accurate

> "Technology is the reason why so many of us are still alive to complain about technology"

Kasparov is a good person

to paraphrase: "Even if we lose jobs to AI, we still improve a lot of lives, and that's what matters"

1. Intelligent tech advances from weak toys to useful tools and eventually to disruptive substitutes.
2. Human + machine means finding better ways to combine, better processes, and virtualization of data.
3. Machines will solve bigger and bigger problems. Humans still ask the same questions and define success.
4. Smarter tools are more powerfull and easier to use, requiring less training and retraining.
5. AI is augmented. We aren't being replaced. We're being promoted.

### Life in The Fast Lane - Don't Get Breached, Embeded Security Into Your Developer Journey

1. Only give the necessary permissions
2. Encourage diversity, aka. code review by multiple people
3. Scan for vulnerabilities early! Reduce attack surface & prioritize critical fixes

### Monitor your data like if it was your code

from [SodaData.io](https://sodatata.io)

> "Software crashed, but Data is just wrong"

seems like they're working on an open-source data monitoring tool, but it doesn't seem to be ready yet

it's supposed to support self-learning of what's regular and what's not, and reporting on that basis

[sodadata on github](https://github.com/sodadata/)

### Brave new world of microservices - patterns, ideas, dos and don'ts

SOA != Microservices

LamaPoll is definitely a monolith

Microservices are an optional structure if a heterogenous structure isn't available to you
(e.g. no developers for your architecture available.)

Microservices are great for:
- splitting up services into separate hardware (e.g. one server for orders, the rest for app)
- separating data sores (e.g. poll from results)
- one service breaking shouldn't break other services

Best practices:
- Don't have client-to-microservice connections, but instead client-to-api-gateway connections
- Don't use synchronous requests between microservices, but use asynchronus SeviceBusses
- Have health check apis
- Be bery cautious when getting data from more than 1 microservice
- "Cloud ready apps" = perfect microservice structure

![deployment models](deployment_models.jpg)

![challenges](challenges.jpg)

### When testing makes no sense

basically, think about what you test, and don't be stupid

- keep tests simple
- keep tests focused

### Testing your tests' quality - Introduction to Mutation Testing

[@felix_codes](https://twitter.com/felix_codes) is 17, and a full-stack dev

If code coverage isn't a good measure of test quality, what is?

Mutation testing isn't just testing your code, it's mutation your code to make existing tests fail.

The more tests fail, the better, since mutated tests should fail.

Tyepes of mutants:
- Value (a=12 -> a=15)
- Operator (a > 2 -> a < 2)
- Statement (a++; -> a++;a++;)

Cons of mutation testing:
- giant amount of mutants increases time the tests take
- equivalent mutants (semantic change, but result stays the same) increase test time without being valuable

Tools for mutation testing:
- [pitest for java](pitest.org)
- stryker for js
- inferno for php

### Bridging the integration gap: How to enable service-rich applications faster and with less code

The gist of the talk seems to be:
Use already existing open source projects and stitch them together, that way you don't have to write them yourself.

The entire talk felt like an ad for:
1. you need an integration platform
2. our integration platform is great

---

## Friday

### Building ethical software

Coding isn't ethics-neutral

> The future is here, but it's distributed unevenly.

![the future is unevenly distributed](future.jpg)

> We can celebrate to good outcomes, but we have a duty to take responsibility for the negative outcomes.

The algorhythms and models you create have a moral weight, and at some point people will be affected by it.

Paper to look at: "Fanning the Flames of Hate: Social Media and Hate Crime"

> Just because we CAN build something, doesn't mean we SHOULD

### Company Culture & Diversity

Great talk, but mostly just personal anecdotes speaking to the people.
Since i'm deep in the topic already, it's not exactly relevant.

### 25 Years of PHP

Seems to be the same talk he held before.

TODO: Check out weak references & FFI in PHP 7.4

Rasmus confirms that it's gif, not jif

> No innovation matters more than that which saves lives.

![dreamers, hackers, coders](dreamershackerscoders.jpg)

### Bulletproof Shoes

Slack tokens:
- xoxp-* = User token
- xoxb-* = Bot token

General rules:
- Clear communication -> It needs to be clear WHY a token has been revoked
- Don't wait till someone reports a token, take precautions instead

about 80% of the tokens they found were valid

### Cyber Hygiene vs. Data Breaches: In a Layman's term

Tools to check for publicly available data:
- Shodan
- Zoomeye
- BinaryEdge
- Censys
- RiskIQ Analysis

We already know HIBP (thanks troy)

Important rules:
1. Know your database documentation, especially best practices re: security
2. Add Firewalls / Access Control Lists
3. Throw away logs when not needed anymore
4. Don't use MD5 hashes (sha-1 is next to be broken, btw)

### Improve the quality of your PHPUnit tests with Infection

Key points:
- Write tests
- Cover mutants
- Repear

### data, design, code

The previous talk (building a data-oriented future) ended 20 minutes later than planned,
so there wasn't really time for us to visit this one.

BUT, the intro made d3.js look quite interesting.

Maik also mentioned processing.js, which supposedly is quite similar.

### Software Quality without Testing

![Quality without testing](quality.jpg)

### Making less of the web with feature policy

[@triblondon](https://twitter.com/triblondon)

[also on github](https://github.com/triblondon)

> How can we fix the web without completely replacing it?

Goals for the future of the web
- Allow good practices to be declared, recognized, and rewarded
- Protect openness and decentralisation
- Do it collaboratively
- Don't break anything

Feature policy is
- a HTTP header
- developer-controlled
- a statement of conformance
- an open standard

[featurepolicy.info](https://featurepolicy.info)

To discover feature policy violations, attach a ReportingObserver via js, or attach a Report-To HTTP header.

You can also set a feature policy that says not to enforce feature policies, but just report them.

There's a [blog post](https://fastly.com/blog/feature-policy-webs-missing-guardrails) containing pretty much all the info from the slides

### 1+1>2 : impacts of pair programming

Didn't really say anything that wasn't obvious before

## Non-talk notes
- Sentry seems very interesting
    - Platform for error reporting, consolidation, and management
    - Open source
    - Self-hosting is possible

How to presentations
1. Start with a quote
2. Think of a powerful statement to capture people
3. Ask a question
4. Give an anecdote/story

Two babies born on the same day, same mom, same dad, not twins. How?

They're triplets.
