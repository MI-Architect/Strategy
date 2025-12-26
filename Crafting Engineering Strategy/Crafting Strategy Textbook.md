This file is a merged representation of a subset of the codebase, containing specifically included files, combined into a single document by Repomix.
The content has been processed where empty lines have been removed.

# File Summary

## Purpose
This file contains a packed representation of the entire repository's contents.
It is designed to be easily consumable by AI systems for analysis, code review,
or other automated processes.

## File Format
The content is organized as follows:
1. This summary section
2. Repository information
3. Directory structure
4. Multiple file entries, each consisting of:
  a. A header with the file path (## File: path/to/file)
  b. The full contents of the file in a code block

## Usage Guidelines
- This file should be treated as read-only. Any changes should be made to the
  original repository files, not this packed version.
- When processing this file, use the file path to distinguish
  between different files in the repository.
- Be aware that this file may contain sensitive information. Handle it with
  the same level of security as you would the original repository.

## Notes
- Some files may have been excluded based on .gitignore rules and Repomix's configuration
- Binary files are not included in this packed representation. Please refer to the Repository Structure section for a complete list of file paths, including binary files
- Only files matching these patterns are included: llm/*.md
- Files matching patterns in .gitignore are excluded
- Files matching default ignore patterns are excluded
- Empty lines have been removed from all files

## Additional Info

# Directory Structure
```
llm/
  01000_preface-strategy-book.md
  02000_intro-strategy.md
  03000_is-strategy-useful.md
  04000_who-gets-to-do-strategy.md
  06000_components-eng-strategy.md
  06000_when-write-strategy.md
  06500_components-eng-strategy.md
  07000_exploring-for-strategy.md
  08000_diagnosis-for-strategy.md
  09000_refining-strategy.md
  10000_policy-for-strategy.md
  11000_operations-for-strategy.md
  12000_organizing-eng-strategy-docs.md
  13000_bridging-theory-and-practice.md
  14000_more-refinement-techniques.md
  15000_testing-strategy.md
  16000_strategy-systems-modeling.md
  17000_wardley-mapping.md
  18000_intro-ds-strategy-part.md
  18000_more-refinement-techniques.md
  19000_uber-service-migration-strategy.md
  20000_uber-service-systems-model.md
  21000_wardley-compute-llm.md
  22000_llm-adoption-strategy.md
  23000_dx-llm-model.md
  24000_wardley-llm-ecosystem.md
  25000_driver-onboarding-model.md
  26000_private-equity-takeover-strategy.md
  27000_eng-cost-model.md
  28000_customer-data-access-strategy.md
  28500_strategy-decompose-monolith.md
  29000_calm-product-eng-company.md
  30000_resource-eng-driven-projects.md
  31000_pos-acquisition-strategy.md
  32000_api-deprecation-strategy.md
  32100_api-deprecation-model.md
  33000_strategy-decompose-monolith.md
  33000_stripe-sorbet.md
  34000_pos-acquisition-strategy.md
  34000_stripe-sorbet.md
  35000_good-vs-bad-strategy.md
  35000_is-this-strategy-good.md
  37000_how-to-get-better-at-strategy.md
  40000_strategy-notes.md
```

# Files

## File: llm/01000_preface-strategy-book.md
````markdown
# Preface
url: https://craftingengstrategy.com/preface

In 2015, the Mini Sky City skyscraper, with 57 floors, was built in Changsha, China, in 19 days. Driving to work over the past few years, I’ve watched a nine-story building in San Francisco get built over three years. There’s some argument that Mini Sky City’s record isn’t legitimate because it relied heavily on modular, pre-built architecture, but I can assure you that the three-years-and-counting building in San Francisco is similarly being built from modular components.
Why did one of these projects build three floors per day, and the other three floors per year?

*[How Big Things Get Done](https://www.amazon.com/How-Big-Things-Get-Done-ebook/dp/B0B3HS4C98/)* by Bent Flyvbjerg and Dan Gardner explores how strategy impacts the successful creation of complex buildings, and their foundational observation is that you go fast by making most of your mistakes where it’s cheapest–for example, in simulation–and fewer where it’s difficult to fix–for example, after you’ve built most of a physical building.
In my experience, their observation applies equally well to software engineering strategy.

However, the problem in software engineering goes further.
You'll never meet an architect who hasn't seen a building plan,
but the majority of software engineers and even software executives will tell you that they’ve never seen a clear, written engineering strategy.
There’s a widespread belief that engineering strategy doesn’t exist, but if you ask the right questions, you’ll find that almost every engineer has a strong instinctive understanding of their current company’s engineering strategy.
Even if that strategy isn't particularly good, they'll know what it is.

This book wants to reshape the conversation around software engineering strategy in two ways. First, I hope to establish a sufficiently clear, shared definition of engineering strategy so that we agree on what we’re talking about.
With that definition, we can start the discussion examining how to improve our strategies, rather than debating whether they exist.
My second goal is to make it easier for all of us to take up the pen to write down our companies’ engineering strategies.
If this book is particularly successful, a few years from now the ideas in this book will be obsolete through their own ubiquity.
They’ll be so obvious that they’re not worth discussing--that would be a triumph

Strategy is often viewed as the dominion of Staff-plus engineers and executives. I hope those folks think a lot about strategy, but this book believes that strategy is applicable–and improvable–by everyone within an engineering organization. If you work within an engineering organization, or even adjacent to an engineering organization, then this book wants to help you understand and improve on your company’s engineering strategy. Certainly, different roles require different approaches, but *you* can contribute to improvement.

Finally, I believe a bit of rigor in our thinking can change our lives, our colleagues' lives, and the lives of the people who
use the software that we create.
Engineering organizations today routinely waste dozens or hundreds of years of their teams’ lives by refusing to engage
with the reality of their problems.
Far from an abstract and aspirational endeavor, strategy is the bare minimum we owe ourselves, our colleagues and our users
to invest our scarce time wisely.

## What This Book is Not

This book is intended to be widely accessible, particularly so for
anyone working in, or adjacent, to software engineering.
However, this book certainly won't be everything to everyone,
and I want to acknowledge some of its limitations.

First, the examples in this book are rooted in my personal experiences.
I've done many things in my career, from starting a small iOS gaming startup in 2008,
to growing Calm's engineering organization, to contributing to
Stripe and Uber's periods of rapid growth. Of course, my experience has its gaps.
I worked at Yahoo! when it was quite large with a massive codebase, but I was there in a junior role,
and I consequently have an incomplete view of working at a company of that size.
I've also never worked in government. Indeed, the list of things I haven't done is endless.

Second, this book is an opinionated introduction to engineering strategy,
and is intended to serve as your first introduction to that hopelessly broad topic.
If you're looking for a more general book on strategy, particularly
if you don't work in a software engineering adjacent field, I'd probably suggest you instead start with
Rumelt's _[Good Strategy, Bad Strategy](https://www.amazon.com/Good-Strategy-Bad-Difference-Matters/dp/0307886239)_.

Finally, this book touches on software architecture a number of times, as software architecture
is a common topic within engineering strategies. However, it is not a book about software architecture.
Where one strategy will focus on software architecture, the next will focus just as heavily on managerial
mechanisms like approving headcount backfills.
For a book on architecture, I might suggest
_[Fundamentals of Software Architecture: An Engineering Approach](https://www.amazon.com/Fundamentals-Software-Architecture-Comprehensive-Characteristics/dp/1492043451)_
by Mark Richards and Neal Ford.

## Navigating This Book

The default way to read this book is to start at the beginning, and read through to the end.
If you do that, you'll work through the book's five parts in order:

* **Part 1: Introducing engineering strategy** introduces this book's overall thesis
* **Part 2: Steps for building engineering strategies** breaks down step-by-step instructions
    for following each of the steps to craft, implement and operate an engineering strategy
* **Part 3: Refine strategy: test, model & map** goes into further detail on the topic of strategy refinement,
    which I believe is the most valuable and most neglected element of engineering strategy
* **Part 4: Strategy case studies** provides ten concrete engineering strategies, all of which are
    based on concrete work I've done in my career (although some are lightly anonymized)
* **Part 5: Going forward** wraps up the book with advice for evaluating strategy, and improving your own strategy work

If you want a more focused dive into the book, I'd encourage you to start by reading the case studies,
and then selectively reading the chapters to understand any parts that you find interesting or surprising.
Reading this way will mean that you're left without some of the relevant definitions,
but realistically most strategy readers are working without those definitions as well,
so hopefully it's still a coherent read.

## Acknowledgments

Each book is the culmination of the prior writing I have done, the people I have had the chance to collaborate with,
and the work itself that has educated me despite my best efforts.
Thank you to each person who has helped me with this book itself, and the work it stands on.

Above all else, I owe indefinite thanks to my wife, Laurel, and my son, Emerson.
Thank you both for being part of this book's journey, and the much
larger journey where this book is only a very small chapter.
````

## File: llm/02000_intro-strategy.md
````markdown
# Introduction
url: https://craftingengstrategy.com/intro

I've worked alongside many talented people who spent years waiting for a chance to finally "do strategy."
My hope is this book convinces you—and maybe them—that waiting is optional.
Strategy isn’t reserved for executives.
It's the art of making thoughtful decisions, and is accessible to everyone--including you.

Even if you'd prefer to avoid strategy, it's still happening all around you.
My first big dose of strategy came managing the team responsible for
[Uber's service migration](https://craftingengstrategy.com/uber-strategy/),
where we desperately tried to survive accelerating inbound requests for support.
Since then, I've seen strategy everywhere I worked, from
[Stripe's acquisition of Index](https://craftingengstrategy.com/index-acquisition-strategy/) to
[Calm's focusing on being a product engineering company](https://craftingengstrategy.com/product-eng-strategy/).
There are even some strategy problems that I've encountered again and again at every company I've joined,
such as [deciding how to decompose monolithic codebases](https://craftingengstrategy.com/monolith-decomposition-strategy/).

This book is focused on engineering strategy.
In other words, making thoughtful decisions about engineering.
"Engineering" is defined both as the discipline of writing software,
and also concerns of the Engineering organization within your company.
If this seems like a hopelessly broad topic, then we agree on the scope of my definition.
However, I would never agree it's hopeless.

My decision making has significantly improved over the course of my career.
I believe very strongly that my improvement had very little to do
with _me_, and a lot to do with learning to engage in structured thinking.
I also believe the lessons that I learned slowly are eminently teachable
in the next couple hundred pages.

## Grounded in my direct experience

Strategy is a broad topic, and many strategy books become awkwardly abstract.
To avoid falling into that trap, I've anchored this book in my personal experiences doing
strategy and the strategy work of colleagues that I had the opportunity to witness directly.

As much as possible, I've used examples that I worked on in real companies,
and I've mentioned those companies by name. That's true for more than half the strategies included in this book,
which describe strategies I collaborated on during my time at Stripe, Uber, and Calm.
For the other half of the strategies, I have abstracted away from specific companies because they are sensitive topics
such as [how to work with private equity ownership](https://craftingengstrategy.com/private-equity-strategy/),
or expose internal information better kept private as in
[how to manage access to customer data](https://craftingengstrategy.com/user-data-strategy/).
In both sorts of examples, I've worked hard to remain honest, even when I've had to omit some details,
out of respect for the companies and individuals involved.

You'll also notice that I've tried to be positive about all of these strategies.
If it seems that I've been too positive, it's because all strategies age.
Even the best strategies eventually turn sour.
It's most interesting to understand strategies in the context they were originally conceived.
Of course, evaluation matters too, which we'll cover in the chapter on [evaluating strategy quality](https://craftingengstrategy.com/evaluating-strategy/).

## Adapting Rumelt for engineering

In addition to my own experience, the second largest influence on this book is
Richard Rumelt’s _[Good Strategy, Bad Strategy](https://www.amazon.com/dp/B004J4WKEC)_.
It's a quick read, and was a life-changing discovery for me.
Rumelt describes three pillars of effective strategy:

1. *Diagnosis* \- a theory describing the nature of the challenge. This involves identifying the root cause(s) at play, for example “high work-in-progress is preventing us from finishing any tasks, so we are increasingly behind each sprint” might be a good diagnosis
2. *Guiding policy* \- a series of general policies which will be applied to grapple with the challenge. Guiding policies are typically going to be implicit or explicit tradeoffs. For example, a guiding policy might be “only hire for most urgent team, do not spread hires across all teams.” If a guiding policy doesn’t imply a tradeoff, you should be suspicious of it. “Working harder to get it done” isn’t really a guiding policy, the relevant guiding policy there might be “work folks hard and expect high attrition”
3. *Coherent actions* \- a set of specific actions directed by guiding policy to address the challenge. This is the most important part, and I think the most exciting part, because it clarifies that a strategy is only meaningful if it leads to aligned action

The first time I read this definition was eye-opening: it answered so many strategy questions I'd had for such a long time.
However, although I was grateful to Rumelt for giving me my first framework for thinking about strategy,
I continued noticing how little deliberate strategy existed in the engineering organizations I'd joined.

Eventually, I recognized that if Rumelt's work was trivial to apply to engineering,
we'd see a lot more disciplined engineering strategy in practice.
We'd also, one hopes, see fewer obviously flawed engineering strategies.
This book is the culmination of my past decade spent understanding how to
adapt Rumelt's approach to something that not only _could_ work,
but concretely _has_ worked in the organizations that I've joined.

## Iterative, intellectual *and* mechanical

In addition to anchoring in my personal experience and building on Richard Rumelt's approach,
there are three characteristics that underpin this book's approach:
being iterative, and embracing both the intellectual and the mechanical aspects of strategy.

Even my proudest strategy work has eventually become obsolete.
For some time, I was embarrassed by this realization.
Eventually, I came to recognize that entropy is natural in strategy work;
good strategy embraces change rather than fights it.
This solidified into the concept of [strategy refinement](https://craftingengstrategy.com/refine/),
where ideas are deliberately validated and improved rather than treated as immutable.

If you've ever participated in an executive hiring loop, you've probably interviewed
someone who described strategic thinking as a personal strength.
Those candidates often draw a distinction between directing how work should be done,
and being in the weeds of doing the work itself.
It happens enough that you start to appreciate that
many people view strategy as a fundamentally intellectual endeavor about how things ought to work,
rather than a mechanical endeavor that studies how things actually do work in practice.

While strategy does indeed have intellectual elements,
effective strategy is at least equally dependent on the mechanical nuances of reality as it is on intellectual frameworks.
Even the best [policies](https://craftingengstrategy.com/policy/) will fail without attention to whether the team is actually adopting the policy's guidance.
Similarly, very effective [operational mechanisms](https://craftingengstrategy.com/operations/) to roll out a strategy
won't help your company if the policy being rolled out is a bad one.

As obvious as these ideas seem, many organizations expect strategies to manifest
perfectly into existence from the very beginning.
This book discusses how to bridge the gap between that pressing expectation of perfection
and the reality that effective strategy
development is grounded in iterative work that is both intellectual and mechanical.

## This book's ambition

As I've worked on this book, one of my lingering concerns
is that the ideas in it are perhaps simply too obvious to write down.
Each time I've been tempted to set the project aside, I see a new example,
or am reminded of an old experience, where some of the smartest people I've
ever known have struggled unsuccessfully with a strategy problem that some people
would describe as quite simple.

The belief that strategy is complex often gets people in trouble.
It's appealing to believe that strategies fail due to detailed
errors in decision-making, or the unanticipated move of an adversary.
Maybe that is common when it comes to grand strategy.
However, my experience is that engineering strategies fail for very mundane reasons.
The most common of these mundane reasons is that executives assume their
strategy will roll itself out. The second is forgetting to spend time
validating the details. Both are avoidable with a bit of structure.

This book's framework is not an attempt to discredit all other approaches. Rather, it's a synthesis
of the various approaches I've encountered, along with a few dimensions that
I've not seen addressed in much detail elsewhere.
Even if you don't agree with my framework, I hope it helps you refine your own framework.
Either way, our industry will be much better for it.
````

## File: llm/03000_is-strategy-useful.md
````markdown
# Is engineering strategy useful?
url: https://craftingengstrategy.com/is-useful

While I frequently hear engineers bemoan a missing strategy,
their complaints rarely articulate why the missing strategy matters.
Instead, it serves as more of a truism: the economy used to be better,
children used to respect their parents,
and engineering organizations used to have an engineering strategy.

This chapter starts by exploring something I believe quite strongly:
there's _always_ an engineering strategy, even if there's nothing written down.
From there, we'll discuss why strategy, especially written strategy, is such
a valuable opportunity for organizations that take it seriously.

We'll dig into:

* Why there's always a strategy, even when people say there isn't
* How strategies have been impactful across my career
* How inappropriate strategies create significant organizational pain without much compensating impact
* How written strategy drives organizational learning
* The costs of not writing strategy down
* How strategy supports personal learning and development,
    even in cases where you're not empowered to "do strategy" yourself

By this chapter's end, hopefully you will agree with me
that strategy is an undertaking worth investing your--and your organization's--time in.

## There's always a strategy

I've never worked somewhere where people didn't claim there was no strategy.
In many of those companies, they'd say there was no engineering strategy.
Once I became an executive and was able to document and distribute an engineering strategy,
accusations of missing strategy didn't go away; they just shifted to focus on a missing
product or company strategy.

This even happened at companies that definitively had engineering strategies like Stripe
in 2016 which had numerous pillars to a clear engineering strategy such as:

* Maintain backwards API compatibility, at almost any cost
    (e.g. force an upgrade from TLS 1.2 to TLS 1.3 to retain PCI compliance,
    but don't force upgrades from the [/v1/charges](https://docs.stripe.com/api/charges/create) endpoint
    to the [/v1/payment_intents](https://docs.stripe.com/api/payment_intents) endpoint)
* Work in Ruby within a monorepo, unless it's the PCI environment, data processing, or data science work
* Engineers are fully responsible for the usability of their work, even when there are
    product or engineering managers involved

Working there it was generally clear what the company's engineering strategy was on any given topic.
That said, it sometimes required asking around, and over time certain decisions became sufficiently
contentious that it became hard to definitively answer what the strategy was.
For example, the adoption of Ruby versus Java became contentious enough that I
distributed a strategy attempting to mediate the disagreement, [Magnitudes of exploration](https://lethain.com/magnitudes-of-exploration/),
although it wasn't a particularly successful effort
(for reasons that are obvious in hindsight, particularly the lack of any enforcement mechanism).

In the same sense that William Gibson said
"The future is already here – it’s just not very evenly distributed,"
there is always a strategy embedded into an organization's decisions,
although in many organizations that strategy is only visible to a small
group, and may be quickly forgotten.

If you ever find yourself thinking that a strategy doesn't exist,
I'd encourage you to instead ask yourself where the strategy lives if you can't find it.
Once you do find it, you may also find that the strategy is quite ineffective,
but I've simply never found that it doesn't exist.

## Strategy _is_ impactful

In ["We are a product engineering company!"](https://craftingengstrategy.com/product-eng-strategy/), we discuss Calm's engineering strategy
to address pervasive friction within the engineering team. The core of that strategy is clarifying how Calm
makes major technology decisions, along with documenting the motivating goal steering those decisions:
maximizing time and energy spent on creating their product.

That strategy reduced friction by eliminating the cause of ongoing debate. It was successful in resetting
the team's focus. It also caused several engineers to leave the company, because it was
incompatible with their priorities.
It's easy to view that as a downside, but I don't think it was.
A clear, documented strategy made it clear to everyone involved what sort of game we were playing,
the rules for that game, and for the first time let them accurately decide if they wanted to be
part of that game with the wider team.

Creating alignment is one of the ways that strategy makes an impact, but
it's certainly not the only way. Some of the ways that strategies
support the organization are:

* **Concentrating company investment into a smaller space.**
    
    For example, [deciding not to decompose a monolith](https://craftingengstrategy.com/monolith-decomposition-strategy/)
    allows you to invest the majority of your tooling efforts on one language,
    one test suite, and one deployment mechanism.
* **Many interesting properties only available through universal adoption.**
    
    For example, moving to an ["N-1 policy" on backfilled roles](https://craftingengstrategy.com/private-equity-model/)
    is a significant opportunity for managing costs, but only works if consistently adopted.
    As another example, many strategies for disaster recovery or multi-region are only viable
    if all infrastructure has a common configuration mechanism.
* **Focus execution on what truly matters.**

    For example, [Stripe's Sorbet strategy](https://craftingengstrategy.com/stripe-sorbet-strategy/) allowed a team of ten engineers
    to incrementally move the company's Ruby monolith towards static typing, without distracting
    the larger organization with the push.
    This was a difficult project, that could have consumed the entire organization for many months, but
    focus allowed a small team to accomplish the majority of early work.
* **Creating a knowledge repository of how your organization thinks.**
    Onboarding new hires, particularly senior new hires, is much more effective with documented strategy.
    
    For example, the [strategy for accessing user data](https://craftingengstrategy.com/user-data-strategy/) requires that all
    access to user data is supported by a clear, user-understandable rationale for that access.
    While this might be obvious to new hires from larger companies,
    folks with only small company experience are likely to be completely unaware this is necessary.
    If it isn't documented, compliance to the policy will quickly decline.

There are some things that a strategy, even a cleverly written one, cannot do.
However, it's always been my experience that developing a strategy creates progress,
even if the progress is understanding the inherent disagreement.

## Inappropriate strategy is especially impactful

While good strategy can accomplish many things, it sometimes feels that inappropriate strategy is far more impactful.
Of course, impactful in all the wrong ways.
[Digg V4](https://lethain.com/digg-v4/) remains the worst considered strategy I've personally participated in.
It was a complete rewrite of the Digg V3.5 codebase from a PHP monolith to a PHP frontend and backend of a dozen Python services.
It also moved the database from sharded MySQL to an early version of Cassandra.
Perhaps worst, it replaced the nuanced algorithms developed over a decade with a hack implemented a few days before
launch.

Although it's likely Digg would have struggled to become profitable due to its reliance on search engine optimization for traffic,
and Google's frequently changing search algorithm of that era, the engineering strategy ensured we died fast
rather than having an opportunity to dig our way out.

Importantly, it's not just Digg. Almost every engineering organization you drill into will have its share of
unused platform projects that captured decades of engineering years to the detriment of an important opportunity.
A shocking number of senior leaders join new companies and initiate a [grand migration](https://lethain.com/grand-migration/)
that attempts to entirely rewrite the architecture, switch programming languages, or otherwise shift their
new organization to resemble a prior organization where they understood things better.

<div class="bg-light-gray br4 ph3 pv1">

**Inappropriate versus bad**

When I first wrote this section, I just labeled this sort of strategy as "bad."
The challenge with that term is that the same strategy might well be very effective
in a different set of circumstances. For example, if Digg had been a three person
company with no revenue, rewriting from scratch could have the right decision!

As a result, I've tried to prefer the term "inappropriate" rather than "bad"
to avoid getting caught up on whether a given approach _might_ work in other
circumstances. Every approach undoubtedly works in _some_ organization.

</div>

## Written strategy drives organizational learning

When I joined Carta, I noticed we had an inconsistent approach
to a number of important problems. Teams had distinct standard kits
for how they approached new projects. Adoption of existing internal platforms
was inconsistent, as was decision making around funding new internal platforms.
There was widespread agreement that we were in the process of decomposing our monolith,
but no agreement on how we were doing it.

Coming into such a [permissive strategy](https://craftingengstrategy.com/when-write-stratefy/) environment,
with strong, differing perspectives on the ideal path forward, one of my first projects
was writing down an explicit engineering strategy along with our newly formed Navigators
team, itself a part of our new engineering strategy.

<div class="bg-light-gray br4 ph3 pv1">

**Navigators at Carta**

As discussed in [Navigators](https://lethain.com/navigators/), we developed a program at Carta to have
explicitly named individuals who are technical leaders to represent key parts
of the engineering organization. This representative leadership group made it possible
to iterate on strategy with a small team of about ten engineers who represented the entire organization,
rather than take on the impossible task of negotiating with 400 engineers directly.

</div>

This written strategy made it possible to explicitly describe the problems we saw,
and how we wanted to navigate those problems. Further, it was an artifact that we
were able to iterate on in a small group, but then share widely for feedback from
teams we might have missed.

After initial publishing, we shared it widely and talked about it frequently in engineering
all-hands meetings. Then we came back to it each year, or when things stopped making much sense,
and revised it. As an example, our initial strategy didn't talk about artificial intelligence at all.
A few months later, we extended it to mention a very conservative approach to using Large Language Models.
Most recently, we've revised the artificial intelligence portion again, as we dive
deeply into [agentic workflows](https://huyenchip.com//2025/01/07/agents.html).

A lot of people have disagreed with parts of the strategy, which is great: that's one
of the key benefits of a written strategy, it's possible to precisely disagree.
From that disagreement, we've been able to evolve our strategy. Sometimes because there's
new information like the current rapid evolution of artificial intelligence practices,
and other times because our initial approach could be improved like in how we gated
membership of the initial Navigators team.

New hires are able to disagree too, and do it from an informed place rather than coming
across as attached to their prior company's practices.
In particular, they're able to understand the historical thinking
that motivated our decisions, even when that context is no longer obvious.
At the time we paused decomposition of our monolith, there was significant friction
in service provisioning, but that's far less true today, which can make the decision
seem a bit arbitrary. Only the written document can consistently communicate that
context across a growing, shifting, and changing organization.

With oral history, what you believe is highly dependent on who you talk with,
which shapes your view of history and the present.
With written history, it's far more possible to agree at scale,
which is the prerequisite to growing at scale rather than isolating
growth to small pockets of senior leadership.

## The cost of implicit strategy

We just finished talking about written strategy, and this book spends a lot of time on this topic,
including [a chapter on how to structure strategies to maximize readability](https://craftingengstrategy.com/readable-strategy/).
It's not _just_ because of the positives created by written strategy, but also because of the damage unwritten strategy
creates.

* **Vulnerable to misinterpretation.**

    Information flow in verbal organizations depends on an individual being in a given room for a decision,
    and then accurately repeating that information to the others who need it.
    However, it's common to see those individuals fail to repeat that information elsewhere.
    Sometimes their interpretation is also faulty to some degree. Both of these create significant
    problems in operating strategy.

<div class="bg-light-gray br4 ph3 pv1">

**Two-headed organizations**

Some years ago, I started moving towards a model where most engineering organizations I worked with
have two leaders: one who's a manager, and another who is a senior engineer. This was partially to
ensure engineering context was included in senior decision making, but it was also to reduce communication errors.

Errors in point-to-point communication are so prevalent when done one-to-one, that the only solution I could
find for folks who weren't reading-oriented communicators was ensuring I had communicated strategy (and other updates) to
at least two people.

</div>

* **Inconsistency across teams.**
    
    At one company I worked in, promotions to Staff-plus role happened at a much higher rate
    in the infrastructure engineering organization than the product engineering team.
    This created a constant drain out of product engineering to work on infrastructure-shaped
    problems, even if those problems weren't particularly valuable to the business.
    
    New leaders had no idea this informal policy existed, and they would routinely
    run into trouble in [calibration discussions](https://lethain.com/perf-management-system/).
    They _also_ weren't aware they needed to go argue for a better policy.
    Worse, no one was sure if this was a real policy or not, so it was ultimately random
    whether this perspective was represented for any given promotion: sometimes
    good promotions would be blocked, sometimes borderline cases would be approved.
* **Inconsistency over time.**
    
    Implementing a new policy tends to be a mix of persistent and one-time actions.
    For example, let's say you wanted to standardize all HTTP operations to use the same
    library across your codebase. You might add a linter check to reject known alternatives,
    and you'll probably do a one-time pass across your codebase standardizing on that library.

    However, two years later there are another three random HTTP libraries in your codebase,
    creeping into the cracks surrounding your linting. If the policy is written down, and a few
    people read it, then there's a number of ways this could be nonetheless prevented.
    If it's not written down, it's much less likely someone will remember,
    and much more likely they won't remember the rationale well enough to argue about it.
* **Hazard to new leadership.**

    When a new Staff-plus engineer or executive joins a company,
    it's common to blame them for failing to understand the existing context behind
    decisions. That's fair: a big part of senior leadership is uncovering and understanding context.
    It's also unfair: explicit documentation of prior thinking would have made this much easier for them.

    Every particularly bad new-leader onboarding that I've seen has involved a new leader coming into an unfilled role,
    that the new leader's manager didn't know how to do. In those cases, success is entirely dependent on that new leader's
    ability and interest in learning.

    
In most ways, the practice of documenting strategy has a lot in common
with [succession planning](https://lethain.com/succession-planning/), where the full benefits
accrue to the organization rather than to the individual doing it.
It's possible to maintain things when the original authors are present,
appreciating the value requires stepping outside yourself for a moment
to value things that will matter most to the organization when you're no
longer a member.

<div class="bg-light-gray br4 ph3 pv1">

**Information herd immunity**

A frequent objection to written strategy is that no one reads anything.
There's some truth to this: it's extremely hard to get everyone in an organization
to know something. However, I've never found that goal to be particularly important.

My view of information dispersal in an organization is the same as
[Herd immunity](https://en.wikipedia.org/wiki/Herd_immunity):
you don't need everyone to know something, just to have enough people who know
something that confusion doesn't propagate too far.

So, it may be impossible for all engineers to know strategy details,
but you certainly can have every Staff-plus engineer and engineering manager
know those details.

</div>

## Strategy supports personal learning

While I believe that the largest benefits of strategy accrue to the
organization, rather than the individual creating it, I also believe that
strategy is an underrated avenue for self-development.

The ways that I've seen strategy support personal development are:

* **Creating strategy builds self-awareness.**

    Starting with a concrete example, I've worked with several engineers who viewed themselves
    as extremely senior, but frequently demanded that projects were implemented using new programming
    languages or technologies because they personally wanted to learn about the technology.
    Their internal strategy was clear--they wanted to work on something fun--but following
    [the steps to build an engineering strategy](https://craftingengstrategy.com/strategy-steps/) would have
    created a strategy that even they agreed didn't make sense.
* **Strategy supports situational awareness in new environments.**

    [Wardley mapping](https://craftingengstrategy.com/wardley-mapping/) talks a lot about situational awareness
    as a prerequisite to good strategy.
    This is ensuring you understand the realities of your circumstances,
    which is the most destructive failure of new senior engineering leaders.
    By explicitly stating the diagnosis where the strategy applied,
    it makes it easier for you to debug why reusing a prior strategy
    in a new team or company might not work.
* **Strategy as your personal archive.**
    
    Just as documented strategy is institutional memory,
    it also serves as personal memory to understand the
    impact of your prior approaches.
    Each of us is an archivist of our prior work, pulling out the
    most valuable pieces to address the problem at hand.
    Over a long career, memory fades--and motivated reasoning creeps in--but explicit documentation doesn't.

Indeed, part of the reason I started working on this book _now_ rather than later
is that I realized I was starting to forget the details of the strategy work I did
earlier in my career. If I wanted to preserve the wisdom of that era, and ensure I
didn't have to relearn the same lessons in the future, I had to write it now.

## Summary

We've covered why strategy can be a valuable learning mechanism for both your engineering organization
and for you. We've shown how strategies have helped organizations deal with service migrations,
monolith decomposition, and right-sizing backfilling. We've also discussed how inappropriate strategy
contributed to Digg's demise.

However, if I had to pick two things to emphasize as this chapter ends, it wouldn't be any of those
things. Rather, it would be two themes that I find are the most frequently ignored:

1. There's always a strategy, even if it isn't written down.
2. The single biggest act you can take to further strategy in your organization
    is to write down strategy so it can be debated, agreed upon, and explicitly evolved.

Discussions around topics like strategy often get caught up in high prestige activities
like making controversial decisions, but the most effective strategists I've seen make
more progress by actually performing the basics: writing things down, exploring widely
to see how other companies solve the same problem, accepting feedback into their draft
from folks who disagree with them. Strategy _is_ useful, and doing strategy can be simple, too.
````

## File: llm/04000_who-gets-to-do-strategy.md
````markdown
# Who gets to do strategy?
url: https://craftingengstrategy.com/who-does-strategy

If you talk to enough aspiring leaders, you'll become familiar with
the prevalent idea that they need to be promoted before they can
work on strategy.
It's widely accepted as true, but I've found this idea fundamentally incorrect:
you can work on strategy from anywhere in an organization.
It just requires different tactics to do so.

Both _Staff Engineer_ and _The Engineering Executive's Primer_ have chapters
on strategy. While the chapters' contents are quite different, both present
a practical path to advancing your organization's thinking about complex topics.
This chapter explains my belief that
_anyone_ within an organization can make meaningful progress on strategy,
particularly if you are honest about the tools accessible to you
and thoughtful about how to use them.

The themes we'll dig into are:

* How to do strategy as an engineer, particularly an engineer who hasn't
    been given explicit authority to do strategy
* Doing strategy as an engineering executive who is responsible for your
    organization's decision-making
* How you can develop engineering strategy even in difficult situations,
    such as when there's no existing strategy,
    when acknowledging certain problems is politically sensitive,
    or when misaligned incentives make consensus challenging
* If this book's argument is that everyone should do strategy,
    is there anyone who, nonetheless, really should not do strategy?

By the end, you'll hopefully agree that engineering strategy is accessible to
everyone, even though you're always operating within constraints.

## Doing strategy as an engineer

It's easy to get so distracted by an executive's top-down approach to
strategy that you convince yourself that there aren't other approachable
mechanisms to doing strategy. There are!

_Staff Engineer_ introduces an approach I call [Take five, then synthesize](https://staffeng.com/guides/engineering-strategy/),
which does strategy by:

1. Documenting how five current and historical related decisions have been made in your organization.
    This is an extended exploration phase
2. Synthesizing those five documents into a diagnosis and policy.
    You are naming the implicit strategy,
    so it's impossible for someone to reasonably argue you're not empowered
    to do strategy: you're just describing what's already happening

At that point, either the organization feels comfortable with what you've written--which is their current strategy--or
it doesn't in which case you've forced a conversation about how to revise the approach.
Creating awareness is often enough to drive strategic change,
and doing so doesn't require any explicit authorization from an executive to do.

When awareness is insufficient, the other pattern I've found highly effective
in low-authority scenarios is an approach I wrote about in
_An Elegant Puzzle_, and call  [model, document, and share](https://lethain.com/model-document-share/):

1. Model the approach you want others to adopt.
    Make it easy for them to observe how you've changed the way you're doing things.
2. Document the approach, the thinking behind it, and how to adopt it.
3. Share the document around. If people see you succeeding with the approach,
    then they're likely to copy it from you.

You might be skeptical because this is an influence-based approach.
However, as we'll discuss in the next section, even an executive-driven
strategy is highly dependent on influence.

<div class="bg-light-gray br4 ph3 pv1">

**Strategy archaeology**

Vernor Vinge's _[A Deepness in the Sky](https://en.wikipedia.org/wiki/A_Deepness_in_the_Sky)_,
published in 1999, introduced the term software archaeologists,
folks who created functionality by cobbling together millennia
of scraps of existing software.

Although it's a somewhat different usage, I sometimes think of the "take five, then synthesize" approach as
performing strategy archaeology. Simply by recording what has happened in the past,
we make it easier to understand the present, and influence the future.

</div>

## Doing strategy as an executive

The biggest misconception about executive roles, frequently held by
non-executives and new executives who are about to make a series of regrettable
mistakes, is that executives operate without constraints.
That is false: executives have an extremely high number of constraints that
they operate under.
Executives have budgets, CEO visions, peers to satisfy, and a team to motivate.
They can disappoint any of these temporarily, but in long-term they have to satisfy
all of them.

Nonetheless, it is true that executives have more latitude to mandate
and cajole participation in the strategies that they sponsor.
_The Engineering Executive's Primer_'s [chapter on strategy](https://lethain.com/eng-strategies/)
is a brief summary of this entire book, but it doesn't say much about
how executive strategy differs from non-executive strategy.

How the executive's approach to strategy differs from the engineer's
can be boiled down to:

1. Executives can mandate adherence to their strategy, which empowers their policy options.
    An engineer can't prevent the promotion of someone who refused to follow their policy, but an executive can.

    Mandates only matter if there are consequences. If an executive is unwilling to
    enforce consequences for non-compliance with a mandate, the ability to issue a
    mandate isn't meaningful.

    This is also true if they _can't_ enforce a mandate because of lack of support from
    their peer executives.
2. Even if an executive is unwilling to use mandates, they have significant visibility
    and access to their organization to advocate for their preferred strategy.
3. Neither access nor mandates improve an executive's ability to diagnose problems.
    However, both often create the appearance of progress.
    This is why executive strategies can fail so spectacularly and endure so long despite failure.

As a result, my experience is that executives have an easier time doing strategy,
but a much harder time learning how to do strategy well,
and fewer protections to avoid serious mistakes.
Further, the consequences of an executive's poor strategy tend to be
much further reaching than an engineer's.
Waiting to do strategy until you are an executive is a recipe for disaster,
even if it looks easier from a distance.

## Doing strategy in other roles

Even if you're neither an engineer nor an engineering executive,
you can still do engineering strategy.
It'll just require an even more influence-driven approach.

The engineering organization is generally right to believe that they know
the most about engineering, but that's not always true.
Sometimes a product manager used to be an engineer and has
significant relevant experience.
Other times, such as the [early adoption of large language models](https://craftingengstrategy.com/llm-adoption-strategy/),
engineers don't know much either, and benefit from outside perspectives.

## Doing strategy in challenging environments

Good strategies succeed by accurately diagnosing circumstances and picking policies that address those circumstances.
You are likely to spend time in organizations where both of those are challenging due to internal limitations,
so it's worth acknowledging that and discussing how to navigate those challenges.

### Low-trust environment

Sometimes the struggle to diagnose problems is a skill issue.
Being bad at strategy is in some ways the easy problem to solve: just do more strategy work to build expertise.
In other cases, you may see what the problems are fairly clearly, but not know how to acknowledge the problems
because your organization's culture would frown on it.
The latter is a diagnosis problem rooted in low-trust, and does make things more difficult.

The chapter on [Diagnosis](https://craftingengstrategy.com/diagnosis/) recognizes this problem,
and admits that sometimes you have to whisper the controversial parts of a strategy:

> When you’re writing a strategy, you’ll often find yourself trying to choose between two awkward options:
> say something awkward or uncomfortable about your company or someone working within it, or
> omit a critical piece of your diagnosis that’s necessary to understand the wider thinking.
> Whenever you encounter this sort of debate, my advice is to find a way to include the diagnosis, but to reframe it into a palatable statement that avoids casting blame too narrowly.

In short, the solution to low-trust is to translate difficult messages into
softer, less direct versions that are acceptable to state.
If your goal is to hold people accountable, this can feel dishonest or
like a ethical compromise, but the goal of strategy is to make better decisions,
which is an entirely different concern than holding folks accountable for the past.

<div class="bg-light-gray br4 ph3 pv1">

**Karpman Drama Triangle**

Sometimes when the diagnosis seems particularly obvious,
and people don't agree with you,
it's because you are wrong.
When I've been obviously wrong about things I understand well,
it's usually because I've fallen into viewing a situation through the
[Karpman Drama Triangle](https://en.wikipedia.org/wiki/Karpman_drama_triangle),
where all parties are mapped onto roles as persecutor, rescuer, or victim.

</div>

## Poor-judgment environment

Even when you do an excellent job diagnosing challenges,
it can be difficult to drive agreement within the organization
about how to address them.
Sometimes this is due to genuinely complex tradeoffs,
for example in [Stripe's acquisition of Index](https://craftingengstrategy.com/index-acquisition-strategy/),
there was debate about how to deal with Index's Java-based technology stack,
which culminated in a compromise that didn't make anyone particularly happy:

> Defer making a decision regarding the introduction of Java to a later date: the introduction of Java is incompatible with our existing engineering strategy, but at this point we’ve also been unable to align stakeholders on how to address this decision. Further, we see attempting to address this issue as a distraction from our timely goal of launching a joint product within six months.
> 
> We will take up this discussion after launching the initial release.

That compromise is a good example of a difficult tradeoff:
although parties disagreed with the approach, everyone understood
the conflicting priorities that had to be addressed.

In other cases, though, there are policy choices that simply don't
make much sense, generally driven by poor judgment in your organization.
Sometimes it's not poor technical judgment, but poor judgment in choosing
to prioritize one's personal interests at the expense of the company's needs.
Calm's strategy to [focus on being a product-engineering organization](https://craftingengstrategy.com/product-eng-strategy/)
dealt with some aspects of that, acknowledged in its diagnosis:

> We’re arguing a particularly large amount about adopting new technologies and rewrites. Most of our disagreements stem around adopting new technologies or rewriting existing components into new technology stacks. For example, can we extend this feature or do we have to migrate it to a service before extending it? Can we add this to our database or should we move it into a new Redis cache instead? Is JavaScript a sufficient programming language, or do we need to rewrite this functionality in Go?

In that situation, your strategy is an attempt to educate your colleagues
about the tradeoffs they are making, but ultimately sometimes folks will disagree with your
strategy.
In that case, remember that most interesting problems require iterative solutions.
Writing your strategy and sharing it will start to change the organization's mind.
Don’t get discouraged even if that change is initially slow.

### Dealing with missing strategies

The strategy for [dealing with new private equity ownership](https://craftingengstrategy.com/private-equity-strategy/)
introduces a common problem: lack of clarity about what other parts of your own company
want. In that case, it seems likely there will be a layoff, but it's unclear how large
that layoff will be:

> Based on general practice, it seems likely that our new Private Equity ownership will expect us to reduce R&D headcount costs through a reduction.
> However, we don’t have any concrete details to make a structured decision on this, and our approach would vary significantly depending on the size of the reduction.

Many leaders encounter that sort of ambiguity and decide that they cannot move forward with
a strategy of their own until that decision is made.
While it's true that it's inconvenient not to know the details,
getting blocked by ambiguity is _always_ the wrong decision.

Instead you should do what the private equity strategy does: accept that ambiguity
as a fact to be worked around. Rather than giving up, it adopts a series of new policies
to start reducing cost growth by changing their [organization's seniority mix](https://craftingengstrategy.com/private-equity-model/),
and recognizes that once there is clarity on reduction targets that there will be additional actions to be taken.

Whenever you're working on challenging problems, you can always find many reasons to justify not making progress.
Leadership is finding a way to move forward despite those issues. A missing strategy is always part of your
diagnosis, but never a reason that you can't do strategy.

## Who shouldn't do strategy

In my experience, there's almost never a reason why _you_ cannot do strategy,
but there are two particular scenarios where doing strategy probably doesn't make sense.
The first is not a who, but a [when problem](https://craftingengstrategy.com/when-write-stratefy/):
sometimes there is so much strategy already happening, that doing more is a distraction.
If another part of your organization is already working on the same problem,
do your best to work with them directly rather than generating competing work.

The other time to avoid strategy is when you're trying to satisfy an emotional need to make a direct, immediate impact.
Sharing a thoughtful strategy always drives progress, though it's often the slow, incremental progress of changing your organization's beliefs.
Even definitive, top-down strategies from executives are often ignored in pockets of an organization,
and bottoms-up strategy spread slowly as they are modeled, documented and shared.
Embarking on strategy work requires a tolerance for winning in the long-run,
even when there's little progress this week or this quarter.

## Summary

As you finish reading this chapter, my hope is that you also believe
that you can work on strategy in your organization, whether you're
an engineer or an executive.
I also hope that you appreciate that the tools you use vary greatly
depending on who you are within your organization and the culture in which you work.
Whether you need to model or can mandate, there's a mechanism
that will work for you.
````

## File: llm/06000_components-eng-strategy.md
````markdown
# Steps to build an engineering strategy.

**This is a work-in-progress draft!**

Often you'll see a disorganized collection of ideas labeled as a "strategy."
Even when they're dense with ideas, these can be hard to parse, and are a major
reason why most engineers will claim their company doesn't have a clear strategy
even though *all* companies follow some strategy, even if it's undocumented.

This chapter lays out a repeatable, structured approach to creating strategy, covering:

* Why structured steps are useful to developing strategy
* Explore
* Diagnose
* Refine
* Policy
* Operation
* How these five steps fit together into strategy
* Whether these steps are sacred or advisory

When you're done with this chapter, you'll have a structured approach for writing a strategy document.
(It won't necessarily be easy to read though,
if you want to make a readable strategy, read through
[Making engineering strategies more readable](/readable-engineering-strategy-documents/).)





## Why these steps are useful

Many strategies get lost in format issues, or process issues, or are just justifying something that's already decided


## Explore

Experts, experts, experts. Talk to experts.
Talk to peers.

peers. Pull some ideas from other writing on strategy.


For more detail, read the [Exploration chapter](/exploring-for-strategy/).


## Diagnose

Talk to stakeholders.
Assess reality.
Debug previous failures, successes.
Consider: Technical, social, financial, etc.


For more detail, read the [Diagnosis chapter](/diagnosis-for-strategy/).

## Refine (Test, Map & Model)


**INCORPORATE:** I've added the idea of testing to this, and I do think it's one of
the missing special tools. e.g. people usually skip testing and go directly into rollout
before they even pressure test their strategy. This is basically doomed to fail every time.

From organizing:

> Now that we have our initial diagnosis written, it’s useful to refine our understanding of a few of the load-bearing aspects.

Load-bearing is a really critical point, because you're trying to maximize
testing/modeling/mapping energy on the most important areas rather than spending
more time on less essential.


This book will go into a variety of mapping and modeling techniques:

* .
* .

the details of using each specific techniques will be covered individually in dedicated chapters.


Refine: Mapping and modeling to visualize Engineering Strategy
It's rarely written down
Examples from case studies of strategies and how you might see them
Mapping strategies
Intuitive mapping: writing what feels right
Talking to a bunch of people – how most new execs build their model
Wardley mapping
Systems thinking and modeling
Constraint optimization as one subset (e.g. Phoenix Project)
Techniques from Technology Strategy Patterns
Surveying – e.g. ask a bunch of folks

For more detail, read the [Refinement chapter](/refining-eng-strategy/).




## Policy

What are categories of policy?
Need to refer to previous writing to think about this.

Policy: common approaches to solving engineering problems
Overview of Engineering Strategies – what can we learn from the deep-dives
Evaluating policy proposals
Benchmarking & “How big things get done” concepts
Policy Transitions – ‘invalidations of diagnosis and how they lead to major policy transitions, perhaps unexpectedly: transition to GenAI, web to Mobile, web 2.0, …


For more detail, read the [Policy chapter](/policy-for-strategy/).

## Operate

Even the best policies have to be interpreted. There will be new circumstances
its authors never imagined, and you must decide on mechanisms for applying its ideas to new needs.

Good strategies explicitly explain how to operate them:

* what are examples of it being correctly applied?
* how to get exceptions?
* who to ask for advice?

Operation: how to make an engineering strategy real
Processes/mechanisms of operation in case studies
Enforcement mechanisms
CTO
Architects
“Navigators”
Navigators – drafting a blog post on this
https://lethain.com/navigators/ 

For more detail, read the [Operations chapter](/operations-for-strategy/).


## How the steps become strategy

Sections: Explore, Diagnose, Refine (Test, Map & Model), Policy, Operation

**TODO:** Look through these, which are directly copied from https://lethain.com/eng-strategies/ for anything major I missed?



## Is the structure sacrosanct?

TODO: add link to template

I will provide a template.
I think templates are very useful for setting a floor of document quality.
However, they also set an artificial ceiling for quality, because sometimes
the template is a bad fit for a specific problem.

So my advice is: ignore the template if it gets in your way, as long as you
understand the rationale behind each of the sections and the tradeoffs of modifying
the sections.

Here are a few particularly common variations:

* Collapsing _Policy_ and _Operations_ into a single, merged section on
    strategies that are operationally simple,
    for example (link to the LLM strategy sample)


Add link to [Making engineering strategies more readable](/readable-engineering-strategy-documents/)


Quote from: organizing for writing/reading:

> Reiterating a point from [Components of engineering strategy](/components-of-eng-strategy/):
> it's always appropriate to change the structure that you develop or present a strategy,
> as long as you are making a deliberate, informed decision.


## Summary

Now, you know the foundational components of strategy,
and can dive into either working down from specific examples to the details
by starting with template strategy examples like
[How should you adopt LLMs?](/llm-adoption-strategy/)
or you can work bottom up, starting with the details of
how [exploration creates the foundation for an effective strategy](/exploring-for-strategy/).

**todo**: mention See [Bridging theory and practice in engineering strategy](/bridging-eng-strategy-theory-and-practice/).
````

## File: llm/06000_when-write-strategy.md
````markdown
# When to write strategy, and how much?
url: https://craftingengstrategy.com/when-write-stratefy

Even if you believe that strategy is generally useful,
it is difficult to decide that today is the day to start writing engineering strategy.
When you do start writing strategy, it's easy to write so much strategy that
your organization is overwhelmed and ignores your strategy rather than
investing time into understanding it.

Fortunately, these are universal problems, and there are a handful of
useful mental models to avoid both extremes.
This chapter covers:

* when to write strategy, in particular the pain points (like cross-team friction)
    and opportunities (like senior hires) that are good moments to start writing
* how much strategy your organization can tolerate, avoiding the traps of writing so much that it's ignored
    or so little that there's not much impact
* using strategy altitude--how permissive a given strategy is and where it's implemented--to manage the overhead
    that strategies creates
* mechanisms to debug whether you're doing too much or too little strategy work

When you're done reading it, you should have a clear perspective on
when to start writing strategy, determining how many strategies to write,
and using strategy altitude to reduce overhead when you do decide to write a
high-volume of strategies.

## When to write strategy

Shortly after becoming Calm's CTO, I opened a document, titled it “Engineering Strategy”, and then stared into that blank abyss before putting it away for a year.
A year later, I came back and documented three guiding principles: [choose boring technology](https://mcfunley.com/choose-boring-technology), resolve conflict with curiosity, and prefer vendors for commoditized functionality.
These simple statements greatly reduced conflict in decision making, and allowed us to focus more energy on improving our product.
When I started, I'd felt like we needed a clearer strategy, but I just didn't know what to write at that point, so I wrote nothing.

Often writing nothing is the best available choice. Indeed, a common slur against leaders is that they "want to be strategic," implying that they're too focused
on abstract ideas rather than on the concrete needs of today. Behind that allegation is an important
truth: strategy work isn't always the most valuable thing you can spend your time. Sometimes working on
strategy is [just snacking](https://staffeng.com/guides/work-on-what-matters/) to avoid something more important.

Before you start working on strategy, you have to decide whether now is the correct time, which depends
on your organization's current strategic state, the trend of your strategic state over time,
and whether you have enough context to be effective.

The first of those three criteria is the idea of strategic state.
Using the example of [service architecture strategy](https://craftingengstrategy.com/monolith-decomposition-strategy/),
your engineering organization is going to be in one of three strategy states:

1. **Globally consistent**: there is a clearly agreed upon strategy, even if it's not written down. When you ask different members of the team
    how to approach a given problem, you get similar answers.
    
    For example, everyone agrees to write new product functionality in the existing monolithic codebase.
2. **Consistent within teams**: there is a clear strategy within pockets of the organization, but there's some inconsistency
    across pockets.
    
    For example, product engineering believes all new functionality should be in a new service within a shared monorepo,
    but all platform engineering believes new functionality should be implemented in a monolith.
3. **Highly varied**: there's little agreement across individuals within engineering on how to approach problems.
    
    For example, some engineers want to do work in new services in a monorepo, others in new services in polyrepos,
    and some believe in implementing new functionality in an existing monolithic service.

If your organization is globally consistent, then it's unlikely that doing more strategy work will be useful unless
your organization is consistently deciding upon an undesirable approach.
If you're in one of the later two states, then it's likely a useful time to write some strategy.

Even if the current state is good, if the organization is trending towards a worse state, it's a valuable time to start doing strategy work.
Conversely, if the current state is decent, and trending towards something better, it's likely not a valuable opportunity.
There are a handful of recurring causes that can lead to abrupt, sometimes unexpected, shifts in state:

1. How much you are, or aren't, hiring. Uber doubled engineering headcount every six months for four years,
    along with opening many distributed engineering offices, which led to highly varied approaches.
    This also meant that the tenure of most engineers was quite low, driving up inconsistency even more.
2. Whether your newly hired external leaders are more playbook-driven or more responsive to the organization's current context.
    Although it's a known anti-pattern in [executive onboarding](https://lethain.com/first-ninety-days-cto-vpe/),
    many leaders are so desperate to make an early impact that they forget to diagnose their new environment
    before making sweeping changes. This creates a strategy rift between teams aligning with the new direction and teams
    maintaining the existing software and infrastructure.
3. How frequently you have significant organizational changes such as reorganizations or layoffs.
    These events can break the mechanisms that propagate culture, which are the sort of subtle [glue work](https://noidea.dog/glue)
    which often gets ignored in spreadsheet-driven exercises.
4. How effectively you've documented historical decisions, and how well you communicate them during onboarding.
    Some companies drill new hires on how decisions are made, and others expect teams to do the training locally.
    Both approaches can work well. Both can work poorly.

Finally, even if the current state is poor and getting worse, you have to assess whether _you_ understand
the organization well enough to start doing useful strategy work. Many new leaders jump in, make assumptions without testing them,
and [attempt a massive migration](https://lethain.com/grand-migration/). That might _feel_ like an audacious example of driving strategy,
but it's mostly just anxiety or ego wrapped in a gantt chart.

The question to ask yourself is whether you understand the history around the areas you want to change,
the individuals who made the decisions, and the context that made them good decisions at that time.
If you know those things for the areas you're focused on, then you're ready to step into strategy.
If not, it's worth slowing down to build the relationships and context necessary to make your subsequent work useful.

If things could be better, or are trending down, and you know enough about the company to get started, then it's
time to start working on strategy.

## How many strategies?

The next question you'll run into after starting work on strategy is: _how much_ strategy should you undertake?
Is it something about programming language choice? Or service decomposition? Or how you prioritize bugs?
Or is it about data warehouses? What about doing all four at once?

With genuinely infinite potential strategies you could work on, it's hard to decide where to start.
By far the most valuable decision you can make is to [limit work in progress](https://lethain.com/limiting-wip/), even if it means starting smaller than you want.
Generally what I've found effective is to start small, iterate on small pieces until you get them working, and only then move on to something larger.
Limit yourself to developing one or two strategies at a time. This gives you bandwidth to ensure the strategies actually work.

To remain effective while limiting concurrent strategy development, it's important to have a clear, but lightly held, point of view
about where you want to get over time. Having a strategy destination makes it possible for each of these smaller chunks to ladder
up into something larger.

Grounding that in a concrete example: at Uber, we were having reliability and productivity issues
related to the monolithic Python codebase. My team didn't have the ability to forbid commits there, but we did have the ability to
make service provisioning really, really easy. So we created a strategy around making service provisioning and operation as painless
as possible. The strategy aimed to solve a later problem of decomposing and departing the monolith, but we didn't address that directly.
We focused on the first step, believing that it was a necessary prerequisite for the subsequent steps. After we proved out the first step,
it then became possible to work strategy on the subsequent steps.

If we had started with the broader strategy, we might have gotten stuck having an intellectual debate about what should happen in the future,
and required many different teams to buy our future vision without having any concrete step for them to take today. By narrowing down, we were
able to iterate on the prerequisites, and delay building consensus until there was a concrete step we needed folks to take.
At that point, there was no intellectual debate about whether it was possible because most people were already operating as we intended.

One of the challenges with reducing the volume of concurrent strategies is that it appears unambitious.
In the Uber example, we _needed_ to solve development in the monolithic codebase, but instead we were talking about
service provisioning, which from a distance seemed like we'd lost the plot. This is a recurring challenge with effective
strategy development: it can appear overly conservative.
Even though in practice it's usually the fastest solution to the underlying problem, it often comes across as slow or indirect.
Solving the appearance of unambition requires proactive storytelling to your stakeholders to explain
both the incremental initiative and the broader vision it will expand to fill over time.

Sometimes this isn't just a stakeholder problem: it can feel slow to you as well.
In those moments, I try to remember that [friction isn't velocity](https://lethain.com/friction-vs-velocity/) and
think about Digg's engineering strategy when I joined.
We had an extremely clear and consistent architecture (a PHP frontend, Python services, Cassandra for all storage),
but the company still collapsed around us.
A few strategies that work are more valuable than a bunch of strategies, even good ones, in a burning building.

## Strategy altitude

Sometimes you _do_ want to lay out a broad, comprehensive strategy,
and you want to do it quickly. That violates the general rule of developing
one strategy at a time, but there's one helpful idea that can often
make this possible: strategy altitude.

It's easiest to explain this idea by starting with a few examples of
operating at different altitudes:

1. A developer experience team wants to increase code quality.
    They create a mechanism that allows teams to define linting rules
    for their own builds. The developer experience team creates opinionated defaults for teams to adopt,
    but each team is empowered to override those defaults locally.
    
    This is a permissive strategy at the engineering organization altitude.
2. A CTO wants to increase code quality.
    They mandate that every pull request must include a test and that CI/CD should block merging pull requests
    that reduce code coverage.
    
    This is a proscriptive strategy at the engineering organization altitude.
3. A product engineering team wants to decrease security vulnerabilities in their software.
    They tell engineers that it's important to consider a number of security issues when
    implementing software, and includes resources for engineers to educate themselves.
    
    This is a permissive strategy at the team altitude.
4. A product engineering team wants to reduce user-impacting bugs.
    They decide that their planning sprints will schedule bug fixes first,
    and only schedule features after draining the bug backlof.
    
    This is a proscriptive strategy at the team altitude.

Permissive strategies are less expensive than prescriptive strategies, because they require little-to-no enforcement.
Lower-altitude strategies (e.g. team strategies) are less expensive than higher-altitude strategies (e.g. org or company strategies),
because they can rely on local mechanisms for rollout and maintenance rather than oversaturated and lossy mechanisms for wider communication
(e.g. communicating in engineering-wide chat channels is, at best, ineffective).

Pulling these ideas together, the formula to increase
strategy volume, is to either reduce altitude or increase permisiveness. Or both.

Going into a concrete example, when I joined Carta, I worked across engineering to roll out quite a bit of strategy work in the first six months.
Some of this was documenting existing strategy, so it didn't require much adoption overhead.
Other parts were a shift in approach, so we focused on developing permissive strategies.
Every strategy included an escape hatch to support local customization, generally asking
each team's [Navigator](https://lethain.com/navigators/) (a Staff-plus engineer responsible for that area) to override
the strategy as appropriate. There was only one place where I was highly proscriptive, which was around
provisioning new services--there, the escape hatch was more restrictive, requiring escalating to the CTO.

Because we focused on permissive strategies, we were able to cover a broad range of topics at high altitude.
If I'd been more proscriptive, the approach would have certainly failed, even though I might have looked like
a more courageous leader. Annoyingly, looking effective and being effective tend to be only lightly correlated.

## Are you doing too much?

Although many engineers feel that their company doesn't have a clear engineering strategy,
it's my experience that significantly more leaders fail by attempting too much strategy work
than by attempting to do too little.

To debug whether you're doing too much, the most valuable question you can ask
is whether your prior strategy work has impacted the subsequent decisions being made.

If you've shared out a bunch of strategy work, but it doesn't seem to be impacting
how your software is written, then you should scale back.
Instead, focus on getting just a single strategy working well, and deeply understand
what's gone wrong in your prior efforts. Then, and only then, return to your prior
work and fix it. Finally, and only after completing the prior steps, expand further.

You may also be doing good work, but simply overwhelming the organization with too much.
Adopting new approaches is hard, and changing everything at once is overwhelming.
Adjust your strategy altitude to make strategies easier to adopt, and slow down on
adding more until the existing ones have been fully adopted.

## Summary

After reading this chapter, you know when it's effective to write strategy, and how to pace yourself to write
a reasonable volume of strategies. You can use strategy altitude to make strategies easier to
adopt, and can debug whether you're overwhelming your organization with too much strategy work.

If you take nothing else away from this chapter, try to always be working on exactly one strategy.
Doing more feels like progress, but usually fails. Doing less is always a missed opportunity.
````

## File: llm/06500_components-eng-strategy.md
````markdown
# Steps to build an engineering strategy.
url: https://craftingengstrategy.com/strategy-steps

Often you'll see a disorganized collection of ideas labeled as a "strategy."
Even when they're dense with ideas, such documents can be hard to parse, and are a major
reason why most engineers will claim their company doesn't have a clear strategy
even though in my experience, *all* companies follow some strategy, even if it's undocumented.

This chapter lays out a repeatable, structured approach to drafting strategy.
It introduces each step of that approach, which are then detailed further in their respective chapters.
Here we'll cover:

* How these five steps fit together to facilitate creating strategy,
    especially by preventing practitioners from skipping steps that feel awkward or challenging.
* Step 1: Exploring the wider industry's ideas and practices around the strategy you're working on.
    Exploration is understanding what recent research might change your approach,
    and how the state of the art has changed since you last tackled a similar problem.
* Step 2: Diagnosing the details of your problem.
    It's hard to slow down to understand your problem clearly before attempting
    to solve it, but it's even more difficult to solve anything well without
    a clear diagnosis.
* Step 3: Refinement is taking a raw, unproven set of ideas and testing them
    against reality. Three techniques are introduced to support this validation process:
    strategy testing, systems modeling, and Wardley mapping.
* Step 4: Policy makes the tradeoffs and decisions to solve your diagnosis.
    These can range from specifying how software is architected, to how pull requests are reviewed,
    to how headcount is allocated within an organization.
* Step 5: Operations are the concrete mechanisms that translate policy into an active force
    within your organization.
    These can be nudges that remind you about code changes without associated tests,
    or weekly meetings where you study progress on a migration.
* Whether these steps are sacred or are open to adaptation and experimentation,
    including when you personally should persevere in attempting steps that don't
    feel effective.

From this chapter's starting point,
you'll have a high-level summary of each step in strategy creation,
and can decide where you want to read further.

## How the steps become strategy

Creating effective strategy is not the rote incantation of a formula. You can’t merely follow these steps to guarantee that you'll create a great strategy.
However, what I’ve consistently found is that strategies fail more often due to avoidable errors than
from fundamentally unsound thinking.
Busy people skip steps. Especially steps they dislike or have failed at before.

These steps are the scaffolding to avoid those errors.
By practicing routinely, you'll build
powerful habits and intuition around which approach is most appropriate for the current strategy you're working on.
They also help turn strategy into a community practice that you, your colleagues,
and the wider engineering ecosystem can participate in together.

Each step is an input that flows into the next step. Your exploration is the foundation
of a solid diagnosis.
Your diagnosis helps you search the infinite space of policy for what you currently need.
Operational mechanisms help you turn policy into an active force supporting your
strategy rather than an abstract treatise.

If you're skeptical of the steps, you should certainly maintain your skepticism,
but do give them a few tries before discarding them entirely.
You may also appreciate the discussion in the chapter on
[bridging between theory and practice when doing strategy](https://craftingengstrategy.com/theory-and-practice/).

## Explore

Exploration is the deliberate practice of searching through a strategy’s problem and solution spaces before allowing yourself to commit to a given approach.
It's understanding how other companies and teams have approached similar questions, and whether their approaches
might also work well for you. It's also learning why what brought you so much success at your former employer
isn't necessarily the best solution for your current organization.

The [Uber service migration strategy](https://craftingengstrategy.com/uber-strategy/) used exploration
to understand the service ecosystem by reading industry literature:

> As a starting point, we find it valuable to read
> [Large-scale cluster management at Google with Borg](https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/43438.pdf)
> which informed some elements of the approach to Kubernetes, and
> [Mesos: A Platform for Fine-Grained Resource Sharing in the Data Center](https://people.eecs.berkeley.edu/~alig/papers/mesos.pdf)
> which describes the Mesos/Aurora approach.

It also used a [Wardley map](https://craftingengstrategy.com/wardley-mapping/) to explore the cloud compute ecosystem.

![The image is a Wardley map, which represents the components involved in a service provision workflow.

**Axes:**
- **Vertical Axis (Value Chain):** Ranges from Invisible to Visible.
- **Horizontal Axis (Evolution):** Ranges from Genesis to Industrialized.

**Components and Connections:**
1. **Product Engineer:** Positioned in the visible and uncharted area, connecting to "Provision new service."

2. **Service Provisioning Team:** Located slightly higher on the evolution scale, it's connected to "Provision new service," "Route traffic to service," and "Add capacity to provisioned service."

3. **Server Operations Team:** More industrialized, linked to "Add capacity to provisioned service" and "Add server capacity to cluster."

4. **Provision New Service:** Connected to "Service provision request workflow" and located near the visible part of the map.

5. **Route Traffic to Service:** Centrally placed and connected to service orchestration and request routing infrastructure.

6. **Service Provision Request Workflow** and **Service Orchestration Pipeline:** Positioned within the genesis to custom area.

7. **Infrastructure and Technology:**
   - **Puppet & Clusto On-prem**
   - **Mesos/Aurora On-prem**
   - **Mesos/Aurora (or Kubernetes) in Cloud**
   - **Serverless in Cloud**  
   These are sequentially arranged within a boxed area showing evolution over time.

8. **Request Infrastructure:** Connected to request](https://craftingengstrategy.com/static/blog/strategy/wardley-compute-v2.png)

<p class="img-desc i tc f6">Evolution of service orchestration in 2014</p>

For more detail, read the [Exploration chapter](https://craftingengstrategy.com/explore/).

## Diagnose

Diagnosis is your attempt to correctly recognize the context that the strategy needs to solve before deciding on the policies to address that context.
Starting from your exploration's learnings, and your understanding of your current circumstances,
building a diagnosis forces you to delay thinking about solutions until you fully understand your problem's nuances.

A diagnosis can be largely data driven, such as
the [navigating a Private Equity ownership transition strategy](https://craftingengstrategy.com/private-equity-strategy/):

> Our Engineering headcount costs have grown by 15% YoY this year, and 18% YoY the prior year.
> Headcount grew 7% and 9% respectively, with the difference between headcount and headcount costs explained by salary band adjustments (4%),
> a focus on hiring senior roles (3%), and increased hiring in higher cost geographic regions (1%).

It can also be less data driven, instead aiming to summarize a problem,
such as the [Index acquisition strategy](https://craftingengstrategy.com/index-acquisition-strategy/)'s
summary of the known and unknown elements of the technical integration
prior to the acquisition closing:

> We will need to rapidly integrate the acquired startup to meet this timeline. We only know a small number of details about what this will entail. We do know that point-of-sale devices directly operate on payment details (e.g. the point-of-sale device knows the credit card details of the card it reads).
> 
> Our compliance obligations restrict such activity to our “tokenization environment”, a highly secured and isolated environment with direct access to payment details. This environment converts payment details into a unique token that other environments can utilize to operate against payment details without the compliance overhead of having direct access to the underlying payment details.

The approach, and challenges, of developing a diagnosis are
detailed in the [Diagnosis chapter](https://craftingengstrategy.com/diagnosis/).

## Refine (Test, Map & Model)

Strategy refinement is a toolkit of methods to identify which parts of your diagnosis
are most important, and verify that your approach to solving the diagnosis actually works.
This chapter delves into the details of using three methods in particular:
[strategy testing](https://craftingengstrategy.com/strategy-testing/),
[systems modeling](https://craftingengstrategy.com/systems-modeling/),
and [Wardley mapping](https://craftingengstrategy.com/wardley-mapping/).

![The image is a flowchart depicting the process of handling requests in a network system involving a load balancer and a server. Here's a detailed breakdown:

1. **Requests**: 
   - Starts the process. 
   - If successful ("OK"), it moves to the Load Balancer.

2. **Load Balancer**: 
   - Receives requests from "Requests".
   - If successful ("OK"), it forwards them to the Server.
   - If there's an error here, it moves to "Failed Requests".
   - If DNS resolution fails, it routes to "Failed Requests".
   - If a response retries (due to HTTP 529), it loops back to "Requests".

3. **Server**: 
   - Receives requests from the Load Balancer.
   - If successful ("OK"), directs them to "Successful Requests".
   - If there's an error, directs to "Failed Requests".

4. **Successful Requests**: 
   - Indicates requests processed without issues.

5. **Failed Requests**: 
   - Captures any requests that encounter errors during processing, including errors in the load balancer, server errors, and DNS resolution failures.

Arrows depict the flow of requests and label transitions such as "OK" and errors. Colors are consistent (light purple) across all components.](https://craftingengstrategy.com/static/blog/strategy/QualityMentalModels.png)

<p class="img-desc i tc f6">Requests succeeding and failing between a user, load balancer, and server</p>
<p class="tc"><em>An example of a systems modeling diagram.</em></p>

These techniques are also demonstrated in the strategy case studies,
such as the [Wardley map of the LLM ecosystem](https://craftingengstrategy.com/wardley-llm-ecosystem/),
or the [systems model of backfilling roles without downleveling them](https://craftingengstrategy.com/private-equity-model/).

For more detail, read the [Refinement chapter](https://craftingengstrategy.com/refine/).

<div class="bg-light-gray br4 ph3 pv1">

### Why isn't refinement earlier (or later)?

A frequent point of disagreement is that refinement should occur before
the diagnosis. Another is that mapping and modeling are two distinct steps,
and mapping should occur before diagnosis, and modeling should occur
after policy.
A third is that refinement ought to be the final step of strategy,
turning the steps into a looping cycle.
These are all reasonable observations, so let me unpack
my rationale for this structure.

By _far_ the biggest risk for most strategies is not that you
model too early, or map too late, but instead that you simply skip
both steps entirely. My foremost concern is minimizing the required
investment into mapping and modeling such that more folks do these steps at all.
Refining after exploring and diagnosing allows you to concentrate your efforts
on a smaller number of load-bearing areas.

That said, it's common to refine many places in your strategy creation.
You're just as likely to have three small refinement steps as one bigger one.

</div>

## Policy

Policy is interpreting your diagnosis into a concrete plan.
This plan also needs to work, which requires careful study
of what's worked within your company, and what new ideas you've
discovered while exploring the current problem.

Policies can range from providing directional guidance,
such as the [user data controls strategy](https://craftingengstrategy.com/user-data-strategy/)'s
guidance:

> **Good security discussions don’t frame decisions as a compromise between security and usability.** We will pursue multi-dimensional tradeoffs to simultaneously improve security and efficiency. Whenever we frame a discussion on trading off between security and utility, it’s a sign that we are having the wrong discussion, and that we should rethink our approach.
>
> We will prioritize mechanisms that can both automatically authorize and automatically document the rationale for accesses to customer data. The most obvious example of this is automatically granting access to a customer support agent for users who have an open support ticket assigned to that agent. (And removing that access when that ticket is reassigned or resolved.)

To committing not to make a decision until later,
as practiced in the [Index acquisition strategy](https://craftingengstrategy.com/index-acquisition-strategy/):

> Defer making a decision regarding the introduction of Java to a later date: the introduction of Java is incompatible with our existing engineering strategy, but at this point we’ve also been unable to align stakeholders on how to address this decision. Further, we see attempting to address this issue as a distraction from our timely goal of launching a joint product within six months.
> 
> We will take up this discussion after launching the initial release.

This chapter further goes into evaluating policies,
overcoming ambiguous circumstances that make it difficult
to decide on an approach, and developing novel policies.

For full detail, read the [Policy chapter](https://craftingengstrategy.com/policy/).

## Operations

Even the best policies have to be interpreted. There will be new circumstances
their authors never imagined, and the policies may be in effect long after their authors have left
the organization. Operational mechanisms are the concrete implementation of your policy.

The simplest mechanisms are an explicit escalation path,
as shown in [Calm's product engineering strategy](https://craftingengstrategy.com/product-eng-strategy/):

> Exceptions are granted by the CTO, and must be in writing. The above policies are deliberately restrictive. Sometimes they may be wrong, and we will make exceptions to them. However, each exception should be deliberate and grounded in concrete problems we are aligned both on solving and how we solve them. If we all scatter towards our preferred solution, then we’ll create negative leverage for Calm rather than serving as the engine that advances our product.

From that starting point, the mechanisms can get far more complex.
This chapter works through evaluating mechanisms, composing an operational plan,
and the most common sorts of operational mechanisms that I've seen across strategies.

For more detail, read the [Operations chapter](https://craftingengstrategy.com/operations/).

## Is the structure sacrosanct?

When someone's struggling to write a strategy document,
one of the first tools someone will often recommend is a strategy template.
Templates are great: they reduce the ambiguity in an already broad project
into something more tractable.
If you're wondering if you should use a template to craft strategy:
sure, go ahead!

However, I find that well-meaning, thoughtful templates often
turn into lumbering, callous documents that serve no one well.
The secret to good templates is that someone has to own it,
and that person has to care about the template writer first and foremost,
rather than the various constituencies that want to insert requirements
into the strategy creation process.
The security, compliance and cost of your plans matter a great deal,
but many organizations start to layer in more and more requirements
into these sorts of documents until the idea of writing them
becomes prohibitively painful.

The best advice I can give someone attempting to write
strategy, is that you should discard every element of strategy
that gets in your way *as long as* you can explain what that element
was intended to accomplish.
For example, if you're drafting a strategy and you don't find any
operational mechanisms that fit. That's fine, discard that section.
Ultimately, the structure is not sacrosanct, it's the thinking
behind the sections that really matter.

This topic is explored in more detail in the chapter on
[Making engineering strategies more readable](https://craftingengstrategy.com/readable-strategy/).

## Summary

Now, you know the foundational steps to conducting strategy.
From here, you can dive into the details with the strategy case studies
like [How should you adopt LLMs?](https://craftingengstrategy.com/llm-adoption-strategy/)
or you can maintain a high altitude starting with
how [exploration creates the foundation for an effective strategy](https://craftingengstrategy.com/explore/).

Whichever you start with, I encourage you to eventually work through both
to get the full perspective.
````

## File: llm/07000_exploring-for-strategy.md
````markdown
# Exploring
url: https://craftingengstrategy.com/explore

A surprising number of strategies are doomed from inception
because their authors get attached to one particular approach
without considering alternatives that would work better for
their current circumstances.
This happens when engineers want to pick tools solely because
they are trending, and when executives insist on adopting the
tech stack from their prior organization where they felt comfortable.

Exploration is the antidote to early anchoring, forcing you to consider
the problem widely _before_ evaluating any of the paths forward.
Exploration is about updating your priors before assuming the industry
hasn't evolved since you last worked on a given problem.
Exploration is continuing to believe that things can get better
when you're not watching.

This chapter covers:

* The goals of the exploration phase of strategy creation
* When to explore (always first!) and when it makes sense to stop exploring
* How to explore a topic, including discussion of the most common mechanisms:
    mining for internal precedent, reading industry papers and books,
    and leveraging your external network
* Why avoiding judgment is an essential part of exploration

By the end of this chapter, you'll be able to conduct an exploration
for the current or next strategy that you work on.

## What is exploration?

One of the frequent senior leadership anti-patterns I've encountered in my career
is [The Grand Migration](https://lethain.com/grand-migration/), where a new leader declares that
a massive migration to a new technology stack--typically the stack used by their
former employer--will solve every pressing problem.
What's distinguishing about the Grand Migration is not the initially bad selection,
but the single-minded ferocity with which the senior leader pushes for their approach,
even when it becomes abundantly clear to others that it doesn't solve the problem at hand.

These senior leaders are very intelligent, but have allowed themselves to be trapped
by their initial thinking from prior experiences. Accepting those early thoughts as the
foundation of their strategy, they build the entire strategy on top of those ideas,
and eventually there is so much weight standing on those early assumptions that it
becomes impossible to acknowledge the errors.

Exploration is the deliberate practice of searching through a strategy's problem and solution spaces
before allowing yourself to commit to a given approach.
It's understanding how others have approached the same problem recently and in the past.
It's doing this both in trendy companies you admire, and in practical companies that actually resemble yours.

Most exploration will be external to your team, but depending on your company,
much of your exploration might be internal to the company.
If you're in a massive engineering organization of 100,000, there are likely existing internal solutions
to your problem that you've never heard of.
Conversely, if you're in an organization of 50 engineers, it's likely that much of your exploration will be external.

## When to explore

Exploration is the first step of good strategy work.
Even when you want to skip it, you will always regret skipping it,
because you'll inadvertently frame yourself into whatever approach you
focus on first.
Especially when it comes to problems that you've solved
previously, exploration is the only thing preventing you
from over-indexing on your prior experiences.

Try to continue exploration until you know how three similar teams within your company and
three similar companies have recently solved the same problem.
Further, make sure you are able to explain the thinking behind those decisions.
At that point, you should be ready to stop exploring
and move on to the [diagnosis step](https://craftingengstrategy.com/diagnosis/) of strategy creation.

Exploration should always come with a minimum and maximum timeframe:
less than a few hours is very suspicious, and more than a week is
questionable as well.

## How to explore

While the details of each exploration will differ a bit,
the overarching approach tends to be pretty similar across strategies.
After I open up the draft strategy document I'm working on,
my general approach to exploration is:

1. Start throwing in every resource I can think of related to that problem.

    For example, in the [Uber service migration strategy](https://craftingengstrategy.com/uber-strategy/),
    I started by collecting recent papers on Mesos, Kubernetes, and Aurora to understand the
    state of the industry on orchestration.
2. Do some web searching, foundational model prompting, and checking with a few current and prior colleagues
    about what topics and resources I might be missing.

    For example, for the [Calm engineering strategy](https://craftingengstrategy.com/product-eng-strategy/),
    I focused on talking with industry peers on tools they'd used to focus
    a team with diffuse goals.
3. Summarize the list of resources I've gathered, organizing them by which I want to explore,
    and which I won't spend time on but are worth mentioning.

    For example, the [Large Language Model adoption strategy](https://craftingengstrategy.com/llm-adoption-strategy/)'s exploration
    section documents the variety of resources the team explored before completing it.
4. Work through the list one by one, continuing to collect notes in the strategy document.
    When you're done, synthesize those into a concise, readable summary of what you've learned.
    
    For example, the [monolith decomposition strategy](https://craftingengstrategy.com/monolith-decomposition-strategy/)
    synthesizes the exploration of a broad topic into four paragraphs, with links out
    to references.
5. Stop once I generally understand how a handful of similar internal and external teams
    have recently approached this problem.

Of all the steps in strategy creation, exploration is inherently open-ended,
and you may find a different approach works better for you. If you're not sure
what to do, try following the above steps closely.
If you have a different approach that you're confident in--as long as it's not skipping exploration!--then
go ahead and try that instead.

<div class="bg-light-gray br4 ph3 pv1">

While not discussed in this chapter, you can also use some techniques like [Wardley mapping](wardley-mapping/),
covered in the [Refinement chapter](https://craftingengstrategy.com/refine/), to support your exploration phase.
Wardley mapping is a strategy tool designed within a different strategy tradition,
and consequently categorizing it as either solely an exploration tool or a refinement tool
ignores some of its potential uses.

There's no perfect way to do strategy: take what works for you and use it.

</div>

## Mine internal precedent

One of the most powerful forms of strategy is simply documenting
how similar decisions have been made internally: often this is enough
to steer how similar future decisions are made within your organization.
This approach, documented in _Staff Engineer_'s [Write five, then synthesize](https://staffeng.com/guides/engineering-strategy/),
is also the most valuable step of exploration for those working in established companies.

If you are a tenured engineer within your organization,
then it's somewhat safe to assume that you are aware of the
typical internal approaches. Even then, it's worth poking around
to see if there are any related skunkworks projects happening internally.
This is doubly true if you've joined the organization recently, or are distant from the codebase itself.
In that case, it's almost always worth poking around to see what already exists.

Sometimes the internal approach isn't ideal, but it's still superior because it's
already been implemented and there's someone else maintaining it.
In the long-run, your strategy can ride along as someone else addresses the issues
that aren't a perfect fit.

## Using your network

[How should we control access to user data](https://craftingengstrategy.com/user-data-strategy/)'s
exploration section begins with:

> Our experience is that best practices around managing internal access to user data
> are widely available through our networks,
> and otherwise hard to find. The exact rationale for this is hard to determine,

While there are many topics with significant public writing out there,
my experience is that there are many topics where there's very little
you can learn without talking directly to practitioners.
This is especially true for security, compliance, operating at truly large scale,
and competitive processes like optimizing advertising spend.

Further, it's surprisingly common to find that how people publicly describe
solving a problem and how they actually approach the problem are largely divorced.

This is why having a broad personal network is exceptionally powerful,
and makes it possible to quickly understand the breadth of possible solutions.
It also provides access to the practical downsides to various approaches,
which are often omitted when talking to public proponents.

In a recent strategy session, a proposal came up that seemed off to me,
and I was able to text--and get answers to those texts--industry peers
before the meeting ended, which invalidated the room's assumptions about what was
and was not possible.
A disagreement that might have taken weeks to resolve was instead resolved in
a few minutes, and we were able to figure out next steps in that meeting rather
than waiting a week for the next meeting when we'd realized our mistake.

Of course, it's _also_ important to hold information from your network with skepticism.
I've certainly had my network be wrong, and your network never knows how your current
circumstances differ from theirs, so blindly accepting guidance from your network
is never the right decision either.

<div class="bg-light-gray br4 ph3 pv1">

If you're looking for a more detailed coverage on
building your network, this topic has also come up in _Staff Engineer_'s
chapter on [Build a network of peers](https://staffeng.com/guides/network-of-peers/),
and _The Engineering Executive's Primer_'s chapter on
[Building your executive network](https://lethain.com/building-exec-network/).
It feels silly to cover the same topic a third time,
but it's a foundational technique for effective decision making.

</div>

## Read widely; read narrowly

Reading has always been an important part of my strategy work.
There are two distinct motions to this approach: read widely on an ongoing basis to broaden your thinking,
and read narrowly on the specific topic you're working on.

Starting with reading widely, I make an effort each year to read ten to twenty industry-relevant works.
These are not necessarily new releases, but are new releases _for me_.
Importantly, I try to read things that I don't know much about or that I initially disagree with.
Some of my recent reads were
_[Chip War](https://www.amazon.com/Chip-War-Worlds-Critical-Technology/dp/1982172002)_,
_[Building Green Software](https://www.amazon.com/Building-Green-Software-Sustainable-Development/dp/1098150627)_,
_[Tidy First?](https://learning.oreilly.com/library/view/tidy-first/9781098151232/)_, and
_[How Big Things Get Done](https://www.amazon.com/How-Big-Things-Get-Done-ebook/dp/B0B3HS4C98/)_.
From each of these books, I learned something, and over time they've built a series of bookmarks
in my head about ideas that might apply to new problems.

On the other end of things is reading narrowly.
When I recently started working on an AI agents strategy,
the first thing I did was read through Chip Huyen's _[AI Engineering](https://www.amazon.com/AI-Engineering-Building-Applications-Foundation/dp/1098166302)_,
which was an exceptionally helpful survey.
Similarly, when we started thinking about [Uber's service migration](https://craftingengstrategy.com/uber-strategy/),
we read a number of industry papers, including
[Large-scale cluster management at Google with Borg](https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/43438.pdf)
and
[Mesos: A Platform for Fine-Grained Resource Sharing in the Data Center](https://people.eecs.berkeley.edu/~alig/papers/mesos.pdf).

None of these readings had all the answers to the problems I was working on,
but they did an excellent job at helping me understand the range of options,
as well as identifying other references to consult in my exploration.

I'll mention two nuances that will help a lot here.
First, I highly encourage getting comfortable with skimming books.
Even tightly edited books will have a lot of content that isn't
particularly relevant to your current goals, and you should skip
that content liberally.
Second, what you read doesn't have to be books.
It can be blog posts, essays, interview transcripts,
or certainly it can be books.

<div class="bg-light-gray br4 ph3 pv1">

In this context, "reading" doesn't even have to actually be reading.
There are conference talks that contain just as much as a blog
post, and conferences that cover as much breadth as a book.
There are also conference talks without a written
equivalent, such as Dan Na's excellent [Pushing Through Friction](https://blog.danielna.com/talks/pushing-through-friction).

</div>

## Each job is an education

Experience is frequently disregarded in the technology industry,
and there are ways to misuse experience by copying too liberally
the solutions that worked in different circumstances, but
the most effective, and the slowest, mechanism for exploring
is continuing to work in the details of meaningful problems.

You probably won't [choose every job to optimize for learning](https://lethain.com/forty-year-career/),
but it allows you to explore more complex problems over time--recognizing that some
of your prior knowledge will have gone stale along the way--which is uniquely valuable.

## Save judgment for later

As I've mentioned several times, the point of exploration is to go broad
with the goal of understanding approaches you might not have considered,
and invalidating things you initially think are true.
Both of those things are only possible if you save judgment for later:
if you're passing judgment about whether approaches are "good" or "bad",
then your exploration is probably going astray.

As a soft rule, I'd argue that if no one involved in a strategy
has changed their mind about something they believed when you
started the exploration step, then you're not done exploring.
This is _especially_ true when it comes to strategy work by
senior leaders. Their beliefs are often well-justified by
years of experience, but it's unclear which parts of their
experience have become stale over time.

## Summary

At this point, I hope you feel comfortable exploring as the first step
of your strategy work, and understand the likely consequences of skipping
this step.
It's not an overstatement to say that every one of the worst strategic failures I've encountered
would have been prevented by its primary author taking a few days to explore the space before
anchoring on a particular approach.

A few days of feeling slow are always worth avoiding years of misguided efforts.
````

## File: llm/08000_diagnosis-for-strategy.md
````markdown
# Diagnosis
url: https://craftingengstrategy.com/diagnosis

Once you've written your [strategy's exploration](https://craftingengstrategy.com/explore/),
the next step is working on its diagnosis.
Diagnosis is understanding the constraints and challenges your strategy needs to address.
In particular, it’s about slowing yourself down from jumping to solutions
before fully understanding the nuances and constraints of the problem.

If you ever find yourself wanting to skip the diagnosis phase--let's get to the solution already!--then
maybe it's worth acknowledging that every strategy that I've seen fail, did so due to a lazy or inaccurate diagnoses.
It's very challenging to fail with a proper diagnosis, and almost impossible to succeed without one.

The topics this chapter will cover are:

* Why diagnosis forms the foundation of an effective strategy, and how effective policies depend upon it.
    Conversely, how skipping the diagnosis phase consistently ruins strategies
* A step-by-step approach to diagnosing your strategy's circumstances
* How to incorporate data into your diagnosis effectively,
    and where to focus on adding data
* Dealing with controversial elements of your diagnosis,
    such as pointing out that your own executive is one
    of the challenges to solve
* Why it's more effective to view difficulties as part
    of the problem to be solved, rather than a blocking
    issue that prevents making forward progress
* The near impossibility of an effective diagnosis
    if you don't bring humility and self-awareness
    to the process

Into the details we go!

## Diagnosis is strategy's foundation

One of the challenges in evaluating strategy is that, after the fact,
many effective strategies are so obvious that they're pretty boring.
Similarly, most ineffective strategies are so clearly flawed that their
authors look lazy.
That's because, as a strategy is operated, the reality around it becomes clear.
When you're writing your strategy, you don't know if you can convince your colleagues
to adopt a new approach to specifying APIs, but a year later you know very definitively
whether it's possible.

Building your strategy's diagnosis is your attempt to correctly recognize the context that
the strategy needs to solve before deciding on the policies to address that context.
Done well, the subsequent steps of writing strategy often feel like an afterthought,
which is why I think of diagnosis as strategy's foundation.

Where [exploration](https://craftingengstrategy.com/explore/) was an evaluation-free activity,
diagnosis is all about evaluation. How do teams feel today? Why did that project fail?
Why did the last strategy go poorly? What will be the distractions to overcome to make
this new strategy successful?

That said, not all evaluation is equal. If you state your judgment directly, it's easy to dispute.
An effective diagnosis is hard to argue against, because it's
a web of interconnected observations, facts, and data.
Even for folks who dislike your conclusions, the weight of evidence
should be hard to shift.

<div class="bg-light-gray br4 ph3 pv1">

[Strategy testing](https://craftingengstrategy.com/strategy-testing/), explored in the Refinement section,
takes advantage of the reality that it's easier to diagnose by doing than by speculating.
It proposes a recursive diagnosis process until you have real-world evidence that the strategy is working.

</div>

## How to develop your diagnosis

Your strategy is almost certain to fail unless you start from an effective diagnosis,
but how to build a diagnosis is often left unspecified.
That's because, for most folks, building the diagnosis is indeed a dark art: unspecified,
undiscussed, and uncontrollable.
I've been guilty of this as well; _The Engineering Executive's Primer_'s
[chapter on strategy](https://lethain.com/eng-strategies/) is notably silent on how to perform diagnosis.

So, yes, there is some truth to the idea that forming your diagnosis is an emergent, organic process rather
than a structured, mechanical one.
However, over time I've come to adopt a fairly structured approach:

1. **Braindump**, starting from a blank sheet of paper, write down your best understanding of the circumstances that
    inform your current strategy. Then set that piece of paper aside for the moment.
1. **Summarize exploration** on a new piece of paper, review the contents of your [exploration](https://craftingengstrategy.com/explore/).
    Pull in every piece of diagnosis from similar situations that resonates with you.
    This is true for both internal and external works!
    For each diagnosis, tag whether it fits perfectly, or needs to be adjusted for your current circumstances.
    Then, once again, set the piece of paper aside.

3. **Mine for distinct perspectives** on yet another blank page, talking to different stakeholders
    and colleagues who you know are likely to disagree with your early thinking.
    Your goal is not to agree with this feedback. Instead, it's to understand their view.

    _[The Crux](https://www.amazon.com/Crux-How-Leaders-Become-Strategists-ebook/dp/B09G2QXXWX)_
    by Richard Rumelt anchors diagnosis in this approach, emphasizing the importance of "testing, adjusting, and changing the frame, or point of view."
4. **Synthesize views into one internally consistent perspective.**
    Sometimes the different perspectives you've gathered don't mesh well.
    They might well explicitly differ in what they believe the underlying problem
    is, as is typical in tension between platform and product engineering teams.
    The goal is to competently represent each of these perspectives in the diagnosis,
    even the ones you disagree with, so that later on you can evaluate your proposed approach
    against each of them.

    When synthesizing feedback goes poorly, it tends to fail in one of two ways.
    First, the author's opinion shines through so strongly that it renders the author
    suspect.
    Your goal isn’t to agree with every perspective, nor should your diagnosis crown one viewpoint as correct.
    The reader should see detailed perspectives without clearly sensing the author's biases.

    The second common issue is when a group tries to jointly own the synthesis,
    but creates fractured perspectives  rather than a unified one.
    I generally find that having one author who is accountable for representing all views
    works best to address both of these issues.
5. **Test drafts across perspectives.**
    Once you've written your initial diagnosis,
    you want to sit down with the people who you expect to disagree
    most fervently. Iterate with them until they agree that you've
    accurately captured their perspective.
    
    It might be that they
    disagree with some other viewpoints, but they should be able
    to agree that others hold those views. They might argue that
    the data you've included doesn't capture their full reality,
    in which case you can caveat the data by saying that their
    team disagrees that it's a comprehensive lens.
6. **Don't worry about getting the details perfectly right in your initial diagnosis.**
    You're trying to get the right crumbs to feed into the next phase,
    [strategy refinement](https://craftingengstrategy.com/refine/).
    Allowing yourself to be directionally correct, rather than perfectly correct,
    makes it possible to cover a broad territory quickly.
    Getting caught up in perfecting details is an easy way to anchor yourself into one perspective
    prematurely.

At this point, I hope you're starting to predict how I'll conclude any recipe for
strategy creation:
if these steps feel overly mechanical to you, adjust them to something that feels
more natural and authentic. There's no perfect way to understand complex problems.
That said, if you feel uncertain, or are skeptical of your own track record,
I do encourage you to start with the above approach as a launching point.

## Incorporating data into your diagnosis

The diagnosis behind [Stripe's creation of Sorbet](https://craftingengstrategy.com/stripe-sorbet-strategy/)
includes a number of pieces of data to help readers understand their reasoning.
For example, it covers staffing numbers of relevant teams, and the extent of test coverage in the Ruby code base.

If everyone has the same data, and the same assumptions about how that data is likely to change going forward,
then evaluating the strategy becomes vastly simpler.
Data is also your mechanism for supporting or critiquing the various views that
you've gathered when drafting your diagnosis; to an impartial reader, data will speak louder than passion.
If you're confident that a perspective is true, then include a data narrative that
supports it. If you believe another perspective is overstated, then include data that the reader
will require to come to the same conclusion.

Do your best to include data analysis with a link out to the full data,
rather than requiring readers to interpret the data themselves while they are reading.
As your strategy document travels further, there will be inevitable requests for
different cuts of data to help readers understand your thinking, and this is somewhat
preventable by linking to your original sources.

If much of the data you want doesn't exist today,
that's a fairly common scenario for strategy work: if the data to make the decision
easy already existed, you probably would have already made a decision rather than needing to
run a structured thinking process.
The next chapter [on refining strategy](https://craftingengstrategy.com/refine/) covers a number of tools
that are useful for building confidence in low-data environments.

## Whisper the controversial parts

At one time, the company I worked at rolled out a bar raiser program styled after Amazon's,
where there was an interviewer from outside the team that had to approve every hire.
I spent some time arguing against adding this additional step as I didn't understand
what we were solving for, and I was surprised at how disinterested management was
about knowing if the new process actually improved outcomes.

What I didn't realize until much later was that most of the senior leadership distrusted one
of their peers, and had rolled out the bar raiser program solely to create
a mechanism to control that manager's hiring bar when the CTO was disinterested holding
that leader accountable.
(I also learned that these leaders didn't care much about implementing this policy,
resulting in bar raiser rejections being frequently ignored,
but that's a discussion for the [Operations for strategy chapter](https://craftingengstrategy.com/operations/).)

This is a good example of a strategy that _does_ make sense with the full diagnosis,
but makes little sense without it, and where stating part of the diagnosis out loud is
nearly impossible. Even senior leaders are not generally allowed to write a document
that says, "The Director of Product Engineering is a bad hiring manager."

When you're writing a strategy, you'll often find yourself trying to choose between
two awkward options:

1. Say something awkward or uncomfortable about your company or someone working within it
2. Omit a critical piece of your diagnosis that's necessary to understand the wider thinking

Whenever you encounter this sort of debate, my advice is to find a way to include the diagnosis,
but to reframe it into a palatable statement that avoids casting blame too narrowly.
I think it's helpful to discuss a few concrete examples of this,
starting with the strategy for [navigating private equity](https://craftingengstrategy.com/private-equity-strategy/),
whose diagnosis includes:

> Based on general practice, it seems likely that our new Private Equity ownership will expect us to reduce R&D headcount costs through a reduction. However, we don’t have any concrete details to make a structured decision on this, and our approach would vary significantly depending on the size of the reduction.

There are many things the authors of this strategy likely feel about their state of reality.
First, they are probably upset about the fact that their new private equity ownership is likely
to eliminate colleagues. Second, they are likely upset that there is no clear plan around what
they need to do, so they are stuck preparing for a wide range of potential outcomes.
However they feel, they stick to precise, factual statements.

For a second example, we can look to the [Uber service migration strategy](https://craftingengstrategy.com/uber-strategy/):

> Within infrastructure engineering, there is a team of four engineers responsible for service provisioning today. While our organization is growing at a similar rate as product engineering, none of that additional headcount is being allocated directly to the team working on service provisioning. We do not anticipate this changing.

The team didn't _agree_ that their headcount should not be growing,
but it was the reality they were operating in. They acknowledged their reality
as a factual statement, without any additional commentary about that statement.

In both of these examples, they found a professional, non-judgmental way to acknowledge
the circumstances they were solving. The authors would have preferred that the leaders
behind those decisions take explicit accountability for them, but it would have undermined
the strategy work had they attempted to do it within their strategy writeup.

Excluding critical parts of your diagnosis makes your strategies particularly
hard to evaluate, copy or recreate.
Find a way to say things politely to make the strategy effective.
As always, strategies are much more about realities than ideals.

## Reframe blockers as part of diagnosis

When I work on strategy with early-career leaders,
an idea that comes up a lot is that an identified problem
means that strategy is not possible. For example, they might
argue that doing strategy work is impossible at their current
company because the executive team changes their mind too often.

That core insight is almost certainly true, but it's much more
powerful to reframe that as a diagnosis: if we don't find a way
to show concrete progress quickly, and use that to excite the executive team,
our strategy is likely to fail.
This transforms the thing preventing your strategy into a condition
your strategy needs to address.

Whenever you run into a reason why your strategy seems unlikely to work,
or why strategy overall seems difficult, you've found an important piece
of your diagnosis to include. There are never reasons why strategy simply
cannot succeed, only diagnoses you've failed to recognize.

For example, in [Calm's approach to resourcing Engineering-driven projects](https://craftingengstrategy.com/project-resourcing-strategy/),
we knew that the company's informal approach to prioritization wasn't going to change.
Even if we convinced our peers in product management to change how _they_ planned,
we'd still be impacted by the executive team's informal planning which wasn't going to change.
Rather than preventing us from implementing a strategy,
those dynamics clarified what sort of approach could actually succeed.

## The role of self-awareness

Every problem of today is partially rooted in the decisions of yesterday.
If you've been with your organization for any duration at all,
this means that _you_ are directly or indirectly responsible for
a portion of the problems that your diagnosis ought to recognize.

This means that recognizing the impact of your prior actions in your diagnosis is a powerful demonstration
of self-awareness. It also suggests that your next strategy's success is rooted
in your self-awareness about your prior choices.
Don't be afraid to recognize the failures in your past work.
While changing your mind _without_ new data is a sign of chaotic leadership,
changing your mind _with_ new data is a sign of thoughtful leadership.

## Summary

Because diagnosis is the foundation of effective strategy,
I've always found it the most intimidating phase of strategy work.
While I think that's a somewhat unavoidable reality, my hope is
that this chapter has somewhat prepared you for that challenge.

The four most important things to remember are simply:

1. form your diagnosis before deciding how to solve it,
2. try especially hard to capture perspectives you initially disagree with,
3. supplement intuition with data where you can, and
4. accept that sometimes you're missing the data you need to fully understand.

The last piece in particular, is why many good strategies never get shared,
and the topic we'll address in the next chapter on [strategy refinement](https://craftingengstrategy.com/refine/).
````

## File: llm/09000_refining-strategy.md
````markdown
# Refining
url: https://craftingengstrategy.com/refine

In Jim Collins' _[Great by Choice](https://www.amazon.com/Great-Choice-Uncertainty-Thrive-Despite/dp/1847940889/)_,
he develops the concept of [Fire Bullets, Then Cannonballs](https://www.jimcollins.com/concepts/fire-bullets-then-cannonballs.html).
His premise is that you should cheaply test new ideas before fully committing to them.
Your organization can only afford firing a small number of cannonballs, but it can bankroll far more bullets.
Why not use bullets to derisk your cannonballs' trajectories?

This chapter presents a series of concrete techniques that I have personally
used to effectively refine strategies before reaching the cannonball stage.
We'll work through:

* An introduction to the practice of strategy refinement
* Why strategy refinement is the highest impact step of strategy creation
* How mixed incentives often cause refinement to be skipped, even though
    skipping leads to worse organizational outcomes
* Building your personal toolkit for refining strategy by picking from various
    refinement techniques like [strategy testing](https://craftingengstrategy.com/strategy-testing/),
    [systems modeling](https://craftingengstrategy.com/systems-modeling/),
    and [Wardley mapping](https://craftingengstrategy.com/wardley-mapping/)
* Brief introductions to each of those refinement techniques. These provide enough context
    to pick which ones might be useful for the strategy that you're working on
* Survey of anti-patterns that skip refinement or manufacture consent to create the illusion
    of refinement without providing the benefits

Each of the refinement techniques, such as systems modeling, is covered in greater
detail--including concrete applications to specific engineering strategies--in the
refinement section of this book.

## What is strategy refinement?

Most strategies succeed because they properly address narrow problems within a broader strategy.
While fully implementing a strategy to validate it is possible, this approach is typically inefficient and slow.
Worse, it's easy to get so distracted by miscellaneous details that you lose sight
of the levers that will make your strategy impactful.

Strategy refinement is a toolkit of methods to identify those narrow problems that matter most,
and validate that your solutions to those problems will be effective.
The right tool within the toolkit will vary depending on the strategy you're working on.
It might be using Wardley mapping to understand how the ecosystem's evolution will impact your approach.
Or it might be systems modeling to determine which part of a migration is the most valuable lever.
In other cases, it's slowing down committing to your strategy until you've done a narrow test drive
to derisk the pieces you don't quite have conviction in yet.

Whatever tools you've relied on to refine strategy thus far in your work, there
are always new refinement tools to pick up. This book presents a workable introduction to several tools that I find reliably useful,
while providing a broader foundation for deploying other techniques that you
develop towards strategy refinement.

## Does refinement matter?

At Stripe, the head of engineering rolled out agile techniques in one meeting.
This change was aimed at our difficulties with planning in periods longer than a month,
which was becoming an increasing challenge as we started working with enterprise businesses who
wanted us to commit to specific functionality as part of signing their contracts.
On the other hand, the approach worked poorly, because it assumed that the issue was engineering managers
being generally unfamiliar with agile techniques.
The challenge of adoption wasn't awareness, but rather the difficulty of prioritizing asks from  numerous stakeholders
in an environment where saying no was frowned upon.

In this agile rollout, the lack of a shared planning paradigm was a real, apt problem.
However, the solution solved the easiest part of the problem, without addressing the
messier parts, and consequently failed to make meaningful progress.
This happens a surprising amount, and can be largely avoided with a small dose of refinement.

On the opposite end, we created Uber's service adoption strategy exclusively through refinement,
because the infrastructure engineering team didn't have any authority to mandate wider changes.
Instead, we relied on two different kinds of refinement to focus our iterative efforts.
First, we used systems modeling to understand what parts of adoption we needed to focus on.
Second, we used strategy testing to learn by migrating individual product engineering teams
over to the new platform.

In the agile adoption example, failure to refine turned a moderately challenging problem
into a strategy failure.
In the service migration example, focus on refinement translated an extremely difficult problem
into a success.
Refinement is, in my experience, the kernel of effective strategy.

## If it matters, why is it skipped?

When a small team creates a strategy,
a so-called [low-altitude strategies](https://craftingengstrategy.com/when-write-stratefy/),
they almost always spend a great deal of time refining their strategy.
This isn't because most teams believe in refinement.
Rather it's because most teams lack the authority to force others to align with their strategy.
This lack of authority means they must incrementally prove out their approach until other teams or executives believe it's worth aligning with.

High-altitude strategy is typically the domain of executives, who generally have the ability to mandate adoption,
and routinely skip the refinement stage, even when it's inexpensive and is almost guaranteed to make them more successful.
Why is that?
When [executives start a new role](https://lethain.com/first-ninety-days-cto-vpe/), they know making an early impression matters.
They also, unfortunately, know that sounding ambitious often resonates more loudly
than doing good work. So, while they do hope to eventually be effective, early on they kick off
a few aspirational initiatives [like a massive overhaul of the codebase](https://lethain.com/grand-migration/),
believing it'll establish their reputation as an effective leader at the company.

This isn't uniquely an executive failure, it also happens frequently in
[permissive strategy organizations](https://craftingengstrategy.com/when-write-stratefy/)
that require [an ambitious, high-leverage project to get promoted into senior engineering roles](https://staffeng.com/guides/staff-projects/).
For example, you might see a novel approach to networking or authorization implemented in a company, whose adoption fails after solving some easier proof points,
and trace its heritage back to promotion criteria.
In many cases, the promotion will come before the rollout stalls out, disincentivizing the would-be promoted engineer
from worrying too deeply about whether this was net-positive for the organization.
The executive responsible for the promotion rubric will eventually recognize the flaw,
but it's not the easiest tradeoff for them to pick between an organization that innovates too much while empowering individuals
or an organization with little waste but restricted room for creativity.

Another reason refinement can get skipped is that sometimes you're forced to urgently create and commit to a strategy,
usually because your boss tells you to. This doesn't actually prevent refinement--just say you're committed and refine anyway--but
often this interaction turns off the strategist's mind, tricking them into intellectually thinking
they can't change their approach because they've already committed to it.
This is never true, all decisions are up for review with proper evidence,
but it takes a certain courage to refine when those around you are asking
for weekly updates on completing the project.

There's one other important reason that strategy refinement gets skipped:
many people haven't built out a toolkit to perform strategy refinement,
and haven't worked with someone who has a toolkit.

## Building your toolkit

I'm eternally grateful to my father, a professor of economics,
who brought me to a systems modeling workshop in Boston one summer
when I was in high school. This opened my eyes to the wide world of
techniques for reasoning about problems, and systems modeling became
the first tool in my toolkit for strategy refinement.

The section on refinement will go into three refinement techniques in significant detail:
[strategy testing](https://craftingengstrategy.com/strategy-testing/), 
[systems modeling](https://craftingengstrategy.com/systems-modeling/), and
[Wardley mapping](https://craftingengstrategy.com/wardley-mapping/),
as well as surveying a handful of other techniques more common to strategy consultants.
Systems modeling I adopted early, whereas Wardley mapping I only learned while
working on this book.
Few individuals are proficient users of many refinement tools, but it's extraordinarily
powerful to unlock your first tool, and worthwhile to slowly expand your experience
with other tools over time. All tools are flawed, and each is best at illuminating
certain types of problems.

If all of these are unfamiliar, then skim over all of them and pick one that seems
most applicable to a current problem you're working on.
You'll build expertise by trying a tool against many different problems,
and talking through the results with engaged peers.

As you practice, remember that the important thing to share is the learning
from these techniques, and try to avoid getting too caught up in sharing the techniques themselves.
I've seen these techniques meaningfully change strategies,
but I've never seen those changes successfully justified through
the inherent insight of the refinement techniques themselves.

## Strategy testing

Sometimes you'll need a strategy to solve an ambiguous problem,
or a problem where diagnosing the issues blocking progress are poorly understood.
At Carta, one strategy problem we worked on was improving code quality,
which is a good example of both of those. It's difficult to agree on
what code quality is, and it's equally difficult to agree on appropriate,
concrete steps to improve it.

To navigate that ambiguity, we spent relatively little time thinking
about the right initial solution, and a great deal of our time
deploying the [strategy testing](https://craftingengstrategy.com/strategy-testing/) technique:

1. Identify the narrowest, deepest available slice of your strategy.
    Iterate on applying that slice until you see some evidence it's working.
2. As you iterate, identify metrics that help you verify the approach is working.
3. Operate from the belief that people are well-meaning,
    and strategy failures are due to excess friction and poor ergonomics.
4. Keep refining until you have conviction that your strategy’s details work in practice,
    or that the strategy needs to be approached from a new direction.

In this case, we achieved some small wins, funded a handful of specific bets that we believed would improve
the problem long-term, and ended the initiative early without making a large organizational commitment.
You could argue that's a failure, but my experience is quite different: having a problem doesn't mean you
have an elegant solution, and strategy testing helps you validate if the solution's efficiency and ergonomics
are viable.

If you're dealing with a deeply ambiguous problem and there's no agreement on
the nature of the reality you're operating in, strategy testing is a great technique to start with.

## Systems modeling

When you're unsure where leverage points might be in a complex system,
[systems modeling](https://craftingengstrategy.com/systems-modeling/)
is an effective technique to cheaply determine which levers might be
effective. For example, the systems model for [onboarding drivers in a ride-share app](https://craftingengstrategy.com/llm-onboarding-model/)
shows that reengaging drivers who've left the platform matters more than bringing on new drivers
in a mature market.

Similarly, in the Uber service migration example,
systems modeling helped us focus on eliminating upfront steps during service
onboarding, shifting to reasonable defaults and away from forcing teams
to learn the new service platform before it had shown any usefulness to them.

![The image is a flowchart illustrating the process of handling requests in a system architecture. It includes the following components and paths:

1. **Requests**: This is the starting point of the flow.
   - If the request is fine, it proceeds with an "OK" status to the Load Balancer.

2. **Load Balancer**: 
   - If the request is processed correctly, it passes with an "OK" status to the Server.
   - If there is an error, it directs to "Failed Requests."
   - DNS resolution failure also leads to "Failed Requests."

3. **Server**: 
   - If the server processes the request successfully, it moves with an "OK" status to "Successful Requests."
   - If there is an error in the server, it goes to "Failed Requests."

4. **Failed Requests**: Accumulates requests that encounter errors in the Load Balancer, Server, or DNS resolution.

5. **Successful Requests**: Collects requests that are processed successfully.

6. **Error Handling**:
   - If a retry occurs (529 HTTP error), requests are sent from "Failed Requests" back to "Requests."

The flowchart uses purple boxes for each component and gray arrows for error paths.](https://craftingengstrategy.com/static/blog/strategy/QualityMentalModels.png)

<p class="img-desc i tc f6">Systems model of errors in a load balancer</p>

While you can certainly reach these insights without modeling, modeling tends to make
the insights immediately visible.
In cases where your model doesn't immediately illuminate what matters most,
studying how your model's projections conflict with real-world data will guide you
to understand where your assumptions are contorting your understanding of the problem.

If you generally understand a problem, but need to determine where to focus
efforts to make the largest impact, then systems modeling is a valuable technique
to deploy.

## Wardley mapping

Many engineering strategies implicitly make the assumption that the ecosystem we're operating
within is static. However, that's certainly false. Many experienced engineers and engineering leaders
have great judgment, and great intuition, but nonetheless deploy a flawed strategy because they've
anchored on their memory of how things work rather than noticing how things have changed over time.

If, rather than being hit over the head by them, you
want to incorporate these changes into your strategy,
[Wardley mapping](https://craftingengstrategy.com/wardley-mapping/) is a great tool to add to your kit.

Wardley maps allow you to plot users, their needs, and then study how
the solutions to those needs will shift over time.
For example, today there is a proliferation of narrow platforms built on
recent advances in large language models, but [studying a Wardley map of the LLM ecosystem](https://craftingengstrategy.com/wardley-llm-ecosystem/)
suggests that it's likely that this ecosystem will consolidate to fewer, broader platforms
rather than remaining so widely scattered across distinct vendors.

![The image is a Wardley Map, which is used for strategic analysis. It displays various components of a value chain related to machine learning and product development.

### Axes:
- **Y-axis (Value Chain):** From "Invisible" at the bottom to "Visible" at the top.
- **X-axis (Evolution):** From "Genesis" on the left to "Commodity (+utility)" on the right. In between, there are labels for "Custom" and "Product (+rental)".

### Components:
- **Invisible to Visible:**
  - **Eval Repository**
  - **Eval Runner**
  - **Indexing Pipeline**
  - **Search Index**
  - **Agent Workflow Orchestrator**
  - **API Proxy**
  - **LLM Vendor Contract**
  
- **Functions/Capabilities:**
  - **Run evals to maintain product quality**
  - **Provide search index to support RAG (Retrieval-Augmented Generation)**
  - **Support for agents**
  - **Visibility into what is sent to models**
  - **Access to latest models**

### Roles/Entities:
- **Product Engineer**
- **Machine Learning Infrastructure**
- **Security & Compliance**

### Connections:
- Various lines connect different components, indicating dependencies or interactions between them.

The map illustrates how these components and roles evolve from innovative, uncharted areas (Genesis) to highly standardized, commoditized services (Commodity). The connections show relationships and dependencies, highlighting how different](https://craftingengstrategy.com/static/blog/strategy/llm-wardley-1.png)

<p class="img-desc i tc f6">Wardley map of Large Language Model ecosystem</p>

If your strategy involves adopting a highly dynamic technology
such as observability in the 2010s, or if your strategy is intended
to span five-plus years, then Wardley mapping will help
surface how industry evolution will impact your approach.

## Anti-patterns in refinement

We've already discussed why **refinement is often skipped**, which is
the most frequent and most damning refinement anti-pattern.
At Calm, we cargo-culted adoption of decomposing our monolithic codebase
into microservices; we had no reason to believe this was improving developer productivity,
but we continued to pursue this strategy for a year before recognizing that we were suffering
from skipping refinement.

The second most common anti-pattern is creating the impression of strategy refinement
through **manufactured consent**. A new senior leader joined Uber and mandated a complete technical re-achitecture,
justifying this in part through the evidence that a number of internal leaders had adopted the same techniques
successfully on their teams. Speaking with those internal leaders, they themselves were skeptical that the
proposal made sense, despite the fact that their surface-level agreement was being used to convince the wider
organization that they believed in the new approach.

Finally, refinement often occurs, but counter-evidence is discarded because the refining team
is **optimizing for a side-goal** of some sort.
My first team at Yahoo adopted Erlang for a key component of [Yahoo! Build Your Own Search Service](https://lethain.com/datahub/),
which proved to be an excellent solution to our problem of wanting to use Erlang,
but a questionable solution to the core problem at hand.
Only three of the engineers on our fifteen person team were willing to touch the Erlang codebase,
but that counter-evidence was ignored because it was in conflict with the side-goal.

## Summary

This chapter has introduced the concept of strategy refinement, surveyed three common
refinement techniques--strategy testing, systems modeling, and Wardley mapping--and provided
a framework for building your personal toolkit for refinement.
When you're ready to get into more detail,
further in the book there's a section dedicated to the details of applying
these techniques, starting with [strategy testing](https://craftingengstrategy.com/strategy-testing/).
````

## File: llm/10000_policy-for-strategy.md
````markdown
# Setting policy
url: https://craftingengstrategy.com/policy

This book's introduction started by defining strategy as "making decisions."
Then we dug into [exploration](https://craftingengstrategy.com/explore/),
[diagnosis](https://lethain.com/diagnosis-for-strategy), and
[refinement](https://craftingengstrategy.com/refine/).
Those are three chapters where you could argue that we didn't decide anything at all.
Clarifying the problem to be solved is the prerequisite of effective decision making, but eventually decisions do have to be made.
Here in this chapter on policy, and the [following chapter on operations](https://craftingengstrategy.com/operations/), we finally start making some decisions.

In this chapter, we'll dig into:

* How we define policy, and how setting policy differs from operating policy as discussed
    in the next chapter
* The structured steps for setting policy
* How many policies should you set? Is it preferable to have one policy, many policies,
    or does it not matter much either way?
* Recurring kinds of policies that appear frequently in strategies
* Why it's valuable to be intentional about your strategy's altitude,
    and how engineers and executives generally maintain
    different altitudes in their strategies
* Criteria to use for evaluating whether your policies are likely to be impactful
* How to develop novel policies, and why it's rare
* Why having multiple bundles of alternative policies is generally
    a phase in strategy development that
    indicates a gap in your diagnosis
* How policies that ignore constraints sound inspirational,
    but accomplish little
* Dealing with ambiguity and uncertainty created by missing strategies
    from cross-functional stakeholders

By the end, you'll be ready to evaluate why an existing strategy's policies are struggling
to make an impact, and to start iterating on policies for strategy of your own.

## What is policy?

Policy is interpreting your [diagnosis](https://craftingengstrategy.com/diagnosis/) into a concrete plan.
That plan will be a collection of decisions, tradeoffs, and approaches.
They'll range from coding practices, to hiring mandates, to architectural decisions,
to guidance about how choices are made within your organization.

An effective policy solves the entirety of the strategy's diagnosis,
although the diagnosis itself is encouraged to specify which aspects can be ignored.
For example, the [strategy for working with private equity ownership](https://craftingengstrategy.com/private-equity-strategy/)
acknowledges in its diagnosis that they don't have clear guidance on what kind of reduction to expect:

> Based on general practice, it seems likely that our new Private Equity ownership will expect us to reduce R&D headcount costs through a reduction. However, we don’t have any concrete details to make a structured decision on this, and our approach would vary significantly depending on the size of the reduction.

Faced with that uncertainty, the policy simply acknowledges the
ambiguity and commits to reconsider when more information becomes available:

> We believe our new ownership will provide a specific target for Research and Development (R&D) operating expenses during the upcoming financial year planning. We will revise these policies again once we have explicit targets, and will delay planning around reductions until we have those numbers to avoid running two overlapping processes.

There are two frequent points of confusion when creating policies
that are worth addressing directly:

1. Policy is a subset of strategy, rather than the entirety of strategy,
    because policy is only meaningful in the context of the strategy's diagnosis.
    For example, the ["N-1 backfill policy"](https://craftingengstrategy.com/private-equity-model/) makes sense in the context of [new, private equity ownership](https://craftingengstrategy.com/private-equity-strategy/).
    The policy wouldn't work well in a rapidly expanding organization.
    
    Any strategy without a policy is useless, but you'll also find policies without context
    aren't worth much either. This is particularly unfortunate, because so often
    strategies are communicated without those critical sections.
2. Policy describes how tradeoffs should be made, but it doesn't verify how the tradeoffs
    are actually being made in practice.
    The next chapter on operations covers how to inspect an organization's behavior to ensure policies
    are followed.
    
    When reworking a strategy [to be more readable](https://craftingengstrategy.com/readable-strategy/),
    it often makes sense to merge policy and operation sections together.
    However, when drafting strategy it's valuable to keep them separate.
    Yes, you _might_ use a weekly meeting to review whether the policy is being followed,
    but whether it's an effective policy is independent of having such a meeting,
    and what operational mechanisms you use will vary depending on the number of policies
    you intend to implement.

With this definition in mind,
now we can move onto the more interesting discussion of how to set policy.

## How to set policy

Every part of writing a strategy feels hard when you're doing it,
but I personally find that writing policy either feels uncomfortably
easy or painfully challenging. It's never a happy medium.
Fortunately, the exploration and diagnosis usually come together
to make writing your policy simple: although sometimes that simple
conclusion may be a difficult one to swallow.

The steps I follow to write a strategy's policy are:

1. **Review diagnosis** to ensure it captures the most important themes.
    It doesn't need to be perfect, but it shouldn't have omissions so obvious
    that you can immediately identify them.
2. **Select policies** that address the diagnosis.
    Explicitly match each policy to one or more diagnoses that it addresses.
    Continue adding policies until every diagnoses is covered.

    This is a broad instruction, but it's simpler than it sounds because you'll
    typically select from policies [identified during your exploration phase](https://craftingengstrategy.com/explore/).
    However, there certainly is space to tweak those policies,
    and to reapply familiar policies to new circumstances.
    
    If you do find yourself developing a novel policy,
    there's a later section in this chapter, _Developing novel policies_,
    that addresses that topic in more detail.
3. **Consolidate policies** in cases where they overlap or adjoin.
    For example, two policies about specific teams might be generalized into a policy about all teams
    in the engineering organization.
4. **Backtest policy** against recent decisions you've made.
    This is particularly effective if you maintain a [decision log](https://infraeng.dev/decision-log/)
    in your organization.
5. **Mine for conflict** once again, much as you did in developing your diagnosis.
    Emphasize feedback from teams and individuals with a different perspective than your own,
    but don't wholly eliminate those that you agree with.
    Just as it's easy to crowd out opposing views in diagnosis if you don't solicit their input,
    it's possible to accidentally crowd out your own perspective if you anchor too much on others' perspectives.
6. **Consider refinement** if you finish writing, and you just aren't sure your approach works -- that's fine!
    Return to the refinement phase by deploying [one of the refinement techniques](https://craftingengstrategy.com/refine/) to increase your conviction.
    Remember that we _talk_ about strategy like it's done in one pass,
    but almost all real strategy takes many refinement passes.

The steps of writing policy are relatively pedestrian, largely because
you've done so much of the work already in the exploration, diagnosis, and refinement steps.
If you skip those phases, you'd likely follow the above steps for writing policy,
but the expected quality of the policy itself would be far lower.

## How many policies?

Addressing the entirety of the diagnosis is often complex,
which is why most strategies feature a set of policies rather than just one.
The [strategy for decomposing a monolithic application](https://craftingengstrategy.com/monolith-decomposition-strategy/)
is not one policy deciding not to decompose, but a series of four policies:

1. Business units should always operate in their own code repository and monolith.
2. New integrations across business unit monoliths should be done using gRPC.
3. Except for new business unit monoliths, we don’t allow new services.
4. Merge existing services into business-unit monoliths where you can.

Four isn't universally the right number either.
It's simply the number that was required to solve that strategy's diagnosis.
With an excellent diagnosis, your policies will often feel inevitable, and perhaps even boring.
That's great: what makes a policy good is that it's effective, not that it's novel or inspiring.

## Kinds of policies

While there are _so many_ policies you can write, I've found they generally fall into one of four major
categories: approvals, allocations, direction, and guidance. This section introduces those categories.

**Approvals** define the process for making a recurring decision.
This might require invoking an architecture advice process,
or it might require involving an authority figure like an executive.

In the [Index post-acquisition integration strategy](https://craftingengstrategy.com/index-acquisition-strategy/),
there were a number of complex decisions to be made, and the approval mechanism was:

> Escalations come to paired leads: given our limited shared context across teams, all escalations must come to both Stripe’s Head of Traffic Engineering and Index’s Head of Engineering.

This allowed the acquired and acquiring teams to start building trust between each other
by ensuring both were consulted before any decision was finalized.
On the other hand, the [user data access strategy](https://craftingengstrategy.com/user-data-strategy/)'s approval
strategy was more focused on managing corporate risk:

> **Exceptions must be granted in writing by CISO.** While our overarching Engineering Strategy states
> that we follow an advisory architecture process as described in _Facilitating Software Architecture_,
> the customer data access policy is an exception and must be explicitly approved, with documentation, by the CISO. Start that process in the #ciso channel.

These two different approval processes had different goals,
so they made tradeoffs differently. There are so many ways to tweak approval,
allowing for many different tradeoffs between safety, productivity, and trust.

**Allocations** describe how resources are split across multiple potential investments.
Allocations are the most concrete statement of organizational priority, and also articulate
the organization's belief about how productivity happens in teams.
Some companies believe you go fast by swarming more people onto critical problems.
Other companies believe you go fast by forcing teams to solve problems without additional headcount.
Both can work, and teach you something important about the company's beliefs.

The strategy on [Uber's service migration](https://craftingengstrategy.com/uber-strategy/) has two concrete examples
of allocation policies. The first describes the Infrastructure engineering team's
allocation between manual provision tasks and investing into creating a self-service provisioning platform:

> **Constrain manual provisioning allocation to maximize investment in self-service provisioning.** The service provisioning team will maintain a fixed allocation of one full time engineer on manual service provisioning tasks. We will move the remaining engineers to work on automation to speed up future service provisioning. This will degrade manual provisioning in the short term, but the alternative is permanently degrading provisioning by the influx of new service requests from newly hired product engineers.

The second allocation policy is implicitly noted in this strategy's diagnosis,
where it describes the allocation policy in the Engineering organization's higher altitude strategy:

> Within infrastructure engineering, there is a team of four engineers responsible for service provisioning today. While our organization is growing at a similar rate as product engineering, none of that additional headcount is being allocated directly to the team working on service provisioning. We do not anticipate this changing.

Allocation policies often create a surprising amount of clarity for the team,
and I include them in almost every policy I write either explicitly,
or implicitly in a higher altitude strategy.

**Direction** provides explicit instruction on how a decision *must* be made.
This is the right tool when you know where you want to go, and exactly the way
that you want to get there. Direction is appropriate for problems you understand
clearly, and you value consistency more than empowering individual judgment.

Direction works well when you need an unambiguous policy that doesn't leave room for interpretation.
For example, [Calm's policy for working in the monolith](https://craftingengstrategy.com/product-eng-strategy/):

> We write all code in the monolith. It has been ambiguous if new code (especially new application code) should be written in our JavaScript monolith, or if all new code must be written in a new service outside of the monolith. This is no longer ambiguous: all new code must be written in the monolith.
>
> In the rare case that there is a functional requirement that makes writing in the monolith implausible, then you should seek an exception as described below.

In that case, the team couldn't agree on what should go into the monolith.
Individuals would often make incompatible decisions, so creating consistency required removing personal judgment from the equation.

Sometimes judgment is the issue, and sometimes consistency is difficult due to misaligned incentives.
A good example of this comes in [strategy on working with new Private Equity ownership](https://craftingengstrategy.com/private-equity-strategy/):

> We will move to an “N-1” backfill policy, where departures are backfilled with a less senior level.
> We will also institute a strict maximum of one Principal Engineer per business unit.

It's likely that hiring managers would simply ignore this backfill policy if it was stated more
softly, although sometimes less forceful policies are useful.

**Guidance** provides a recommendation about how a decision _should_ be made.
Guidance is useful when there's enough nuance, [ambiguity](https://lethain.com/navigating-ambiguity/), or complexity
that you _can_ explain the desired destination, but you _can't_ mandate the path to reaching it.

One example of guidance comes from the [Index acquisition integration strategy](https://craftingengstrategy.com/index-acquisition-strategy/):

> **Minimize changes to tokenization environment**: because point-of-sale devices directly work with customer payment details, the API that directly supports the point-of-sale device must live within our secured environment where payment details are stored.
>
> However, any other functionality must not be added to our tokenization environment.

This might read like direction, but it's clarifying the desired outcome of avoiding unnecessary complexity
in the tokenization environment. However, it's not able to articulate what complexity is necessary,
so ultimately it's guidance because it requires significant judgment to interpret.

A second example of guidance comes in the [strategy on decomposing a monolithic codebase](https://craftingengstrategy.com/monolith-decomposition-strategy/):

> **Merge existing services into business-unit monoliths where you can.** We believe that each choice to move existing services back into a monolith should be made “in the details” rather than from a top-down strategy perspective. Consequently, we generally encourage teams to wind down their existing services outside of their business unit’s monolith, but defer to teams to make the right decision for their local context.

This is another case of knowing the desired outcome, but encountering too much uncertainty
to direct the team on how to get there. If you ask five engineers about whether it's possible
to merge a given service back into a monolithic codebase, they'll probably disagree.
That's fine, and highlights the value of guidance: it makes it possible to make incremental progress in areas
where more concrete direction would cause confusion.

When you're working on a strategy's policy section, it's important to consider all of these categories.
Which feel most natural to use will vary depending on your team and role, but they're all usable:

* If you're a developer productivity team, you might have to lean heavily on guidance in your policies
    and increased support for that guidance within the details of your platform.
* If you're an executive, you might lean heavily on direction. Indeed, you might lean _too_ heavily on direction,
    where guidance often works better for areas where you understand the direction but not the path.    
* If you're a product engineering organization, you might have to narrow the scope of your direction
    to the engineers within that organization to deal with the realities of complex cross-organization dynamics.

Finally, if you have a clear approach you want to take that doesn't fit cleanly into any of these
categories, then don't let this framework dissuade you. Give it a try, and adapt if it doesn't initially work out.

## Maintaining strategy altitude

The chapter on [when to write engineering strategy](https://craftingengstrategy.com/when-write-stratefy/)
introduced the concept of strategy altitude, which is being deliberate about where
certain kinds of policies are created within your organization.

Without repeating that section in its entirety, it's particularly relevant when
you set policy to consider how your new policies eliminate flexibility within your
organization. Consider these two somewhat opposing strategies:

* [Stripe's Sorbet strategy](https://craftingengstrategy.com/stripe-sorbet-strategy/) only worked in an organization
    that enforced the use of a single programming language across
    (essentially) all teams
* [Calm's strategy for resourcing Engineering-driven projects](https://craftingengstrategy.com/project-resourcing-strategy/)
    knew that resourcing had to be managed by the team directly.
    Attempting to solve the problem at another level would simply result
    in someone talking to the team directly to rewrite their priorities
    to incorporate a new urgent project.

Stripe's organization-altitude policy took away the freedom of individual teams
to select their preferred technology stack. In return, they unlocked the ability
to centralize investment in a powerful way.
Calm went the opposite way, recognizing that only teams were empowered to
manage the contents of their roadmap; executives were more senior, but frequently
overridden by other executives' out-of-band instructions.

Both altitudes make sense. Both have consequences.

## Criteria for effective policies

In _[The Engineering Executive's Primer](https://www.amazon.com/Engineering-Executives-Primer-Impactful-Leadership/dp/1098149483/)_'s
chapter on [engineering strategy](https://lethain.com/eng-strategies/), I introduced three criteria for evaluating policies.
They ought to be applicable, enforced, and create leverage. Defining those a bit:

1. **Applicable**: it can be used to navigate complex, real scenarios, particularly when making tradeoffs.
2. **Enforced**: teams will be held accountable for following the guiding policy.
3. **Create Leverage**: create compounding or multiplicative impact.

The last of these three, create leverage, made sense in the context of a book about
engineering executives, but probably doesn't make as much sense here.
Some policies certainly should create leverage
(e.g. [the policy to avoid deprecating APIs](https://craftingengstrategy.com/api-deprecation-strategy/) makes other customer retention mechanisms more effective)
but others might not
(e.g. [moving to an N-1 backfill policy](https://craftingengstrategy.com/private-equity-strategy/)).
Outside the executive context, what's important isn't necessarily creating leverage,
but that a policy solves for part of the diagnosis.

That leaves the other two--being applicable and enforced--both of which are necessary
for a policy to actually address the diagnosis.
Any policy which you can't determine how to apply, or aren't willing to enforce,
simply won't be useful.

Let's apply these criteria to a handful of potential policies.
First let's think about policies we might write to improve the
talent density of our engineering team:

* **"We only hire world-class engineers."**
    This isn't applicable, because it's unclear what a world-class engineer means.
    Because there's no mutually agreeable definition in this policy, it's also not consistently enforceable.
* **"We only hire engineers that get at least one 'strong yes' in scorecards."**
    This is applicable, because there's a clear definition.
    This is enforceable, depending on the willingness of the organization to reject seemingly good candidates
    who don't happen to get a strong yes.

Next, let's think about a policy regarding code reuse within a codebase:

* **"We follow a strict Don't Repeat Yourself policy in our codebase."**
    There's room for debate within a team about whether two pieces of code are truly
    duplicative, but this is generally applicable.
    Because there's room for debate, it's a very context specific determination to decide how to enforce a decision.
* **"Code authors are responsible for determining if their contributions violate Don't Repeat Yourself, and rewriting them if they do."**
    This is much more applicable, because now there's only a single person's judgment to assess the potential repetition.
    In some ways, this policy is also more enforceable, because there's no longer any ambiguity around who is deciding whether
    a piece of code is a repetition.

    The challenge is that
    enforceability now depends on one individual, and making this policy effective will require
    holding individuals accountable for the quality of their judgement.
    An organization that's unwilling to distinguish between good and bad judgment
    won't get any value out of the policy.
    This is a good example of how a good policy in one organization might become a poor policy in another.

If you ever find yourself wanting to include a policy that for some reason
either can't be applied or can't be enforced, stop to ask yourself what you're
trying to accomplish and ponder if there's a different policy that might be better suited to that goal.

## Developing novel policies

My experience is that there are vanishingly few truly novel policies
to write. There's almost always someone else has already done something similar to your intended approach.
[Calm's engineering strategy](https://craftingengstrategy.com/product-eng-strategy/) is such a case:
the details are particular to the company, but the general approach is common across the industry.

The most likely place to find truly novel policies is during the adoption phase of a new widespread technology,
such as the rise of ubiquitous mobile phones, cloud computing, or large language models.
Even then, as explored in [the strategy for adopting large-language models](https://craftingengstrategy.com/llm-adoption-strategy/),
the new technology can be engaged with as a generic technology:

> **Develop an LLM-backed process for reactivating departed and suspended drivers in mature markets.** Through modeling our driver lifecycle, we determined that improving onboarding time will have little impact on the total number of active drivers. Instead, we are focusing on mechanisms to reactivate departed and suspended drivers, which is the only opportunity to meaningfully impact active drivers.

You could simply replace "LLM" with "data-driven" and it would be equally readable.
In this way, policy can generally sidestep areas of uncertainty by being a bit abstract.
This avoids being overly specific about topics you simply don't know much about.

However, even if your policy isn't novel to the industry,
it might still be novel to you or your organization.
The steps that I've found useful to debug novel policies are the same steps as running a condensed version
of the strategy process, with a focus on exploration and refinement:

1. Collect a number of _similar_ policies, with a focus on how
    those policies differ from the policy you are creating
2. Create a [systems model](https://craftingengstrategy.com/systems-modeling/) to
    articulate how this policy will work,
    and also how it will differ from the similar policies you're considering
3. Run a [strategy testing](https://craftingengstrategy.com/strategy-testing/) cycle
    for your proto-policy to discover any unknown-unknowns about how it
    works in practice

Whether you run into this scenario is largely a function of the extent
of your, and your organization's, experience. Early in my career, I found
myself doing novel (for me) strategy work very frequently, and these days
I rarely find myself doing novel work, instead focusing on adaptation
of well-known policies to new circumstances.

## Are competing policy proposals an anti-pattern?

When creating policy, you'll often have to engage with the question of
whether you should develop one preferred policy or a series of potential strategies to pick from.
Developing these is a useful stage of setting policy, but rather than
helping you refine your policy, I'd encourage you to think of this as
exposing gaps in your diagnosis.

For example, [when Stripe developed the Sorbet ruby-typing tooling](https://craftingengstrategy.com/stripe-sorbet-strategy/),
there was debate between two policies:

1. Should we build a ruby-typing tool to allow a centralized team to gradually
    migrate the company to a typed codebase?
2. Should we migrate the codebase to a preexisting strongly typed language like Golang
    or Java?

These were, initially, equally valid hypotheses. It was only by clarifying our diagnosis
around resourcing that it became clear that incurring the bulk of costs
in a centralized team was clearly preferable to spreading the costs across many teams.
Specifically, recognizing that we wanted to prioritize short-term product engineering velocity,
even if it led to a longer migration overall.

If you do develop multiple policy options, I encourage you to move the alternatives
into an appendix rather than [including them in the core of your strategy document](https://craftingengstrategy.com/readable-strategy/).
This will make it easier for readers of your final version to understand how to follow your policies,
and they are the most important long-term user of your written strategy.

## Recognizing constraints

A similar problem to competing solutions is developing a policy that you cannot possibly fund.
It's easy to get enamored with policies that you can't meaningfully enforce,
but that's bad policy, even if it would work in an alternate universe where it
was possible to enforce or resource it.

To consider a few examples:

* The [strategy for controlling access to user data](https://craftingengstrategy.com/user-data-strategy/) might have proposed
    requiring manual approval by a second party of every access
    to customer data. However, that would have gone nowhere.
* Our [approach to Uber's service migration](https://craftingengstrategy.com/uber-strategy/)
    might have required more staffing for the infrastructure engineering team,
    but we knew that wasn't going to happen, so it was a meaningless policy proposal to make.
* The strategy for [navigating private equity ownership](https://craftingengstrategy.com/private-equity-strategy/) might
    have argued that new ownership should not hold engineering accountable to a new standard
    on spending. But they would have just invalidated that strategy in the next financial planning period.

If you find a policy that contemplates an impractical approach,
it doesn't _only_ indicate that the policy is a poor one,
it also suggests your policy is missing an important pillar.
Rather than debating the policy options, the fastest path to
resolution is to align on the diagnosis that would invalidate
potential paths forward.

In cases where aligning on the diagnosis isn't possible,
for example because you simply don't understand the possibilities
of a new technology as encountered in the [strategy for adopting LLMs](https://craftingengstrategy.com/llm-adoption-strategy/),
then you've typically found a valuable opportunity to use [strategy refinement](https://craftingengstrategy.com/refine/)
to build alignment.

## Dealing with missing strategies

At a recent company offsite, we were debating which policies we might adopt to deal
with annual plans that kept getting derailed after less than a month.
Someone remarked that this would be much easier if we could get the executive team to
commit to a clearer, written strategy about which business units we were prioritizing.

They were, of course, right. It would be much easier. Unfortunately,
it goes back to the problem we discussed in the [diagnosis chapter](https://craftingengstrategy.com/diagnosis/)
about reframing blockers into diagnosis. If a strategy from the company or a peer function is missing,
the empowering thing to do is to include the absence in your diagnosis and move forward.

Sometimes, even when you do this, it's easy to fall back into the belief that you cannot set a policy
because a peer function might set a conflicting policy in the future.
Whether you're an executive or an engineer, you'll never have the details you want to make
the ideal policy. Meaningful leadership requires taking meaningful risks,
which is never something that gets comfortable.

## Summary

After working through this chapter,
you know how to develop policy, how to assemble policies to solve your diagnosis,
and how to avoid a number of the frequent challenges that policy writers encounter.
At this point, there's only one phase of strategy left to dig into,
[operating the policies you've created](https://craftingengstrategy.com/operations/).
````

## File: llm/11000_operations-for-strategy.md
````markdown
# Operations
url: https://craftingengstrategy.com/operations

Even the best policies fail if they aren't adopted by the teams they're intended to serve.
Can we persistently change our company's behaviors with a one-time announcement?
No, probably not.

I refer to the art of making policies work as "operations" or "strategy operations."
The good news is that effectively operating a policy is two-thirds avoiding
common practices that simply don't work.
The other one-third takes some repetition, but can be practiced in any engineering role:
there's no need to wait until you're an executive to start building mastery.

This chapter will dig into those mechanisms, with particular focus on:

* How policies are supported by operations, and how
    operations are composed of mechanisms that ensure they work well
* Evaluating operational mechanisms to select between different options,
    and determine which mechanisms are unlikely to be an effective choice
* Composing an operational plan for the specific set of policies that
    you are looking to support
* Common varieties of effective mechanisms such as approval forums, inspection mechanisms,
    nudges, and so on.
    We'll also explore the sorts of mechanisms that tend to work poorly
* How to adjust your approach to operations if you are in an engineering
    role rather than an executive role
* How cargo-culting remains the largest threat to effective strategy operations

Let's unpack the details of turning your _potentially_
good policy into an impactful policy.

## What are operational mechanisms?

Operations are how a policy is implemented and reinforced.
Effective operations ensure that your policies actually accomplish something.
They can range from a recurring weekly meeting, to an alert that notifies the team when a threshold is exceeded,
to a promotion rubric requiring a certain behavior to be promoted.

In the strategy for [working with new private equity ownership](https://craftingengstrategy.com/private-equity-strategy/),
we introduce a policy to backfill hires at a lower level, and also limit the maximum number
of principal engineers:

> **We will move to an “N-1” backfill policy**, where departures are backfilled with a less senior level.
> We will also institute a strict maximum of one Principal Engineer per business unit,
> with any exceptions approved in writing by the CTO–this applies for both promotions and external hires.

That introduces an explicit operational mechanism of escalations going to the CTO,
but it also introduces an implicit and undefined mechanism: how do we ensure the backfills are actually
down-leveled as the policy instructs?
It might be a group chat with engineering recruiting where the CTO approves the level of backfilled roles.
Instead, it might be the responsibility of recruiting to enforce that downleveling.
In a third approach, it might be taken on trust that hiring managers will do the right thing.
Each of those three scenarios is a potential operational solution to implementing this policy.
Operations is picking the right one for your circumstances, and then tweaking it
as you learn from running it.

<div class="bg-light-gray br4 ph3 pv1">

**Operations in government**

For another interesting take on how critical operations are,
_[Recoding America](https://www.recodingamerica.us/)_ by Jennifer Pahlka
is well worth the read.
It explores how well-intended government legislation often isn't implementable,
which results in policies that require massive IT investments
but provide little benefit to constituents.

</div>

## How to evaluate mechanisms

In order to determine the most effective operational mechanisms
for the problems you're working on, it's useful to have a
standardized rubric for evaluating mechanisms.
While this rubric isn't perfectly universal--customize it for your needs--having
any rubric will make it easier to evaluate your options consistently.

The rubric I use to evaluate whether an operational mechanism will be effective is:

1. **Measurability**:
    Can you measure both leading and lagging indicators
    to [inspect](https://lethain.com/inspection/) the mechanism's impact?
    If you have to choose between the two, measuring leading indicators allows much quicker
    evaluation and iteration on your mechanisms.
2. **Adoption cost**:
    How much work will [migrating](https://lethain.com/migrations/) to this mechanism require?
    Can this work be done incrementally or does it require a major, coordinated shift?
3. **User ease (or burden)**:
    After adopting this policy, how much easier (or harder) will it be for users to perform their work?
    If things will be harder, are those users able to tolerate the additional time?
4. **Provider ease (or burden)**:
    How much additional ongoing maintenance will this mechanism require from the centralized or
    platform team providing it?
    For example, if every new architecture proposal requires a thorough review by your Security team,
    does the Security team have the actual ability to support those reviews?
5. **Reliance on authority**:
    How much does this mechanism depend on a top-down authority's active support?
    If the sponsoring executive departs, will this mechanism remain effective?
    Is that an effective tradeoff in this case?
6. **Culturally aligned**:
    Is this something that your organization is going to do,
    or something that they are going to fight against each step?
    Is there a way you can adjust the framing to make it more acceptable
    to your organization's culture?

Generally, I find folks are good at evaluating mechanisms against these criteria,
but somewhat worse at accepting the consequences of their evaluation.
For example, falling in love with a particular mechanism
and then trying to force the organization to accept a mechanism whose adoption cost is unbearably high,
or introduce a mechanism that creates significant user burden onto a team that is
already struggling with tight efficiency goals like a customer support team.

Self-awareness helps here, but so does consulting others to point out the errors in your reasoning,
which is a core part of how I've found success in adopting operational mechanisms.

## Composing an operational plan

Your operational plan is the sum of the mechanisms used to support your policies.
While evaluating each individual mechanism in isolation is part of creating an operations plan,
it's also valuable to consider how the mechanisms will work together:

1. **Review the policies you've developed.**
    What sort of mechanisms seem most likely to support these policies?
    How might these mechanisms be pooled together to avoid redundancy?
2. **Review the operational mechanisms that have worked in your organization.**
    What mechanisms have been used to best effect, and which have left a sufficiently bad
    taste in the organization's collective memory that they'll be hard to reuse effectively?
3. **Which new mechanisms showed up in your [exploration](https://craftingengstrategy.com/explore/)?**
    In your exploration phase, you'll frequently encounter mechanisms that your organization
    hasn't previously tried. If any of them seem particularly well-suited to the policies
    you're considering, and none of your organization's frequently used mechanisms are good fits,
    then consider testing a new one.
4. **Evaluate mechanisms against the evaluation rubric.**
    For each of the mechanisms you're considering using,
    apply the rubric from the above _How to evaluate mechanisms_
    to validate they're good fits.
5. **Consolidate into an operational plan.**
    Now that you've determined the mechanisms you want to consider,
    work on fitting the full set of mechanisms into one coherent plan.
    Be particularly mindful of the ease, or burden, the integrated plan
    creates for both your users and platform providers.
6. **Validate plan with users and providers.**
    Many plans make sense from afar, but fail
    due to imposing an unreasonable burden.
    Or the burden might be acceptable, but the actual workflow
    simply won't work at all.
7. **Consider validating via [strategy testing](https://craftingengstrategy.com/strategy-testing/).**
    If you run the above process, and can't come to an agreement with stakeholders on your proposed plan,
    then simply commit to running a strategy testing process including the plan.
    This will create space for everyone to build confidence in the approach before
    they feel forced to make a commitment to following it long-term.
    
    Even if you don't use strategy testing for your plan,
    at least commit to scheduling a review in three months
    reflecting on how things have worked out.

Your operational plan is the vehicle that delivers your policies
to your organization. It's extremely tempting to skip refining
the details here, but it's a relatively quick step and will
completely change your strategy's outcomes.

## Common mechanisms

Most companies have a handful of frequently used operational mechanisms.
Some of those mechanisms are company specific, such as [Amazon's weekly business review](https://forum.commoncog.com/t/the-amazon-weekly-business-review-commoncog/1958),
and others repeat across companies like requiring executive approval.
Across the many mechanisms you'll encounter, you can generally cluster them into
recurring categories.
This section covers the mechanisms I've found consistently effective.

### Approval and advice forums

At a high level, new policies are obvious, simple and apply cleanly to the problem they are intended to solve.
However, when you apply those policies to detailed, complex circumstances, it's often ambiguous how
to stay loyal to a policy's intentions.
Approval and advice forums are a common solution to that problem.

[Calm's product engineering strategy](https://craftingengstrategy.com/product-eng-strategy/) shows what the simplest,
and most common, approval forum looks like in practice:

> **Exceptions are granted by the CTO, and must be in writing.** The above policies are deliberately restrictive. Sometimes they may be wrong, and we will make exceptions to them. However, each exception should be deliberate and grounded in concrete problems we are aligned both on solving and how we solve them. If we all scatter towards our preferred solution, then we’ll create negative leverage for Calm rather than serving as the engine that advances our product.
> 
> All exceptions must be written. If they are not written, then you should operate as if it has not been granted. Our goal is to avoid ambiguity around whether an exception has, or has not, been approved. If there’s no written record that the CTO approved it, then it’s not approved.

This example also has several weaknesses that happen in many approval forums.
Most importantly, it doesn't make it clear how to get approvals.
It would be stronger if it explicitly explained how to get an approval (perhaps go ask in `#cto-approvals`),
and where to find prior approvals to help someone considering requesting an exception to
calibrate their request.

Approvals don't necessarily need to come from senior leadership.
Instead, the senior leadership can loan their authority on a topic to another group.
The [LLM adoption strategy](https://craftingengstrategy.com/llm-adoption-strategy/) provides a good example of this:

> Start with Anthropic. We use Anthropic models, which are available through our existing cloud provider via AWS Bedrock. To avoid maintaining multiple implementations, where we view the underlying foundational model quality to be somewhat undifferentiated, we are not looking to adopt a broad set of LLMs at this point. This is anchored in our Wardley map of the LLM ecosystem.
> 
> Exceptions will be reviewed by the Machine Learning Review in #ml-review

In a more community-minded organization, the approval forums might not
require senior leadership involvement at all. Instead, the culture might
create an environment where the forums' feedback is taken seriously on its
own merits.

Every company does approval forums a bit differently, ranging from
our experiments at [Carta with Navigators](https://lethain.com/navigators/), granting executive authority for
technical decisions to named engineers in each area,
to Andrew Harmel-Law's discussion of this topic in
_[Facilitating Software Architecture](https://www.amazon.com/Facilitating-Software-Architecture-Empowering-Architectural-ebook/dp/B0DMHGWCPN/)_.
You can spend a lot of time arguing the details here,
my experience is that having the right participants and a good executive sponsor
matter a lot, and the other pieces matter a lot less.

### Inspection

While even the best policies can fail, the more common scenario is that
a policy will sort-of work, and need some modest adjustments to make it
more successful. An [inspect](https://lethain.com/inspection/) mechanism allows you to evaluate
whether your policy is succeeding and if you need to make adjustments.

The [user-data access strategy](https://craftingengstrategy.com/user-data-strategy/) provides
an example:

> **Measure progress on percentage of customer data access requests justified by a user-comprehensible, automated rationale.** This will anchor our approach on simultaneously improving the security of user data and the usability of our colleagues’ internal tools. If we only expand requirements for accessing customer data, we won’t view this as progress because it’s not automated (and consequently is likely to encourage workarounds as teams try to solve problems quickly). Similarly, if we only improve usability, charts won’t represent this as progress, because we won’t have increased the number of supported requests.
> 
> As part of this effort, we will create a private channel where the security and compliance team has visibility into all manual rationales for user-data access, and will directly message the manager of any individual who relies on a manual justification for accessing user data.

This example is a good start, but fully realizing an inspection mechanism requires concretely specifying where and how the
data will be tracked. A better version of this would include a link to the dashboard you'll look at,
and a commitment to reviewing the data on a certain frequency.

For a recent inspection mechanism, I created a recurring invite with a link to the relevant data dashboard,
and a specific chat channel for discussion, and invited
the working group who had agreed to review the data on that cadence.
This wasn't a synchronous meeting, but rather a commitment to independently review, and discuss anything that felt surprising.

Your particular mechanisms could be threshold-triggered alerts, something you fold into an existing metrics review meeting,
a script you commit to running and reviewing periodically, or something else.
The most important thing is that it cannot silently fail.

### Nudges

While it's common to hear complaints about how a team isn't following a new policy,
as if it were a deliberate choice they'd made, I find it more common that people
want to do things the new way, but rarely take time to learn how to do it.
Nudges are providing individuals with context to inform them about a better way
they might do something, and they are an exceptionally effective mechanism.

Grounding this in an example, at Stripe we had a policy of allowing teams
to self-authorize introducing new cloud hosting costs. This worked well
almost all the time. However, sometimes teams would accidentally introduce
large cost increases without realizing it, and teams that introduced those
spikes almost never had any awareness that they had caused the problem.
Even if we'd told them they must not introduce unapproved spending spikes,
they simply didn't perceive they'd done it.

We had the choice between preventing all teams from introducing new spend,
or we could try using a nudge. The nudge we added informed teams when
their cloud spend accelerated month over month, directed to charts that
explained the acceleration, and told them where to go to ask questions.
Nudges pair well with inspections, and there was also a monthly review
by the Efficiency Engineering team to review any spikes and reach out where necessary.

Maybe we could have forced all teams to review new spend,
but this nudge approach didn't require an authoritative mandate to implement.
It also meant we only spent time advising teams that _actually_ spent too much,
instead of having to discuss with every team that _might_ spend too much.

As another example making that point, a working group at Carta added a nudge to inform managers
of untested pull requests merged by their team. Some managers had previously
said they simply didn't know when and why their team had merged untested pull requests,
and this nudge made it easy to detect. The nudge also respected their attention
by not sending a notification at all if there wasn't a new, untested pull request.

With poor ergonomics, nudges can be an overwhelming assault on your colleagues attention,
but done well, I continue to believe they are the most effective operational mechanism.

### Documentation

Policies can't be enforced by people who don't know they exist,
or by people who don't know how to follow those policies.
In my experience, nudges are the most effective way of solving both of those problems,
because nudges bring information to people at exactly the moment that information would
be useful.
At most companies, well-done nudges are relatively uncommon, and the far more common solution
to lack of information is documentation and training.

There are so many approaches to both of these topics,
and I've not found my own approaches here particularly effective.
Consequently, I am hesitant to give much advice on what will work best
for you.
The best I can offer is that following standard practices for your company,
even if the outcomes seem imperfect, is probably your best bet.
Internal knowledge bases tend to rot quickly, and introducing yet another
knowledge base is almost always the illusion of progress rather than real progress.
Even when you really don't like the current one.

Finally, remember that success for documentation and training is not necessarily
that everyone in the company knows how a new policy works.
Instead, as discussed in [the chapter on whether strategy is useful](https://craftingengstrategy.com/is-useful/),
a more useful goal is informational herd immunity: as long as someone on each team
understands your policy, the team will generally be capable of following it.

### Automation

Relying on humans to respond is slow, and the quality of human response is highly varied.
In many cases, automation provides the most effective and most scalable mechanism
to support your policies' rollout.

Automation was key in the [Uber service migration strategy](https://craftingengstrategy.com/uber-strategy/),
moving us out of a manual, slow process that was taking up a great deal of user and provider time:

> Move to structured requests, and out of tickets. Missing or incorrect information in provisioning requests create significant delays in provisioning. Further, collecting this information is the first step of moving to a self-service process. As such, we can get paid twice by reducing errors in manual provisioning while also creating the interface for self-service workflows.

In that case, better automation allowed us to eliminate a series of back-and-forth negotiations to collect
data, and to instead get the necessary information in a single step. Occasionally we still ran into users who
couldn't fill in the form, but now we could focus on providing a good manual experience for those rare exceptions.

As you use automation as a core strategy mechanism,
it's important to recognize that designing an effective
user experience is a prerequisite to automation having a positive impact.
If you view the user experience of your automation as a secondary concern,
then you are unlikely to make much impact with automation.

### Deferment to future work

Sometimes there's something you really want a policy to do, but you also
know that you have no reasonable mechanism to do it.
In that case, you may find explicitly deferring action on the topic useful.

The strategy for [integration of the Index acquisition at Stripe](https://craftingengstrategy.com/index-acquisition-strategy/)
uses this mechanism:

> Defer making a decision regarding the introduction of Java to a later date: the introduction of Java is incompatible with our existing engineering strategy, but at this point we’ve also been unable to align stakeholders on how to address this decision. Further, we see attempting to address this issue as a distraction from our timely goal of launching a joint product within six months.
> 
> We will take up this discussion after launching the initial release.

As did the strategy for [working with a private equity acquirer](https://craftingengstrategy.com/private-equity-strategy/):

> We believe there are significant opportunities to reduce R&D maintenance investments, but we don’t have conviction about which particular efforts we should prioritize. We will kickoff a working group to identify the features with the highest support load.

There's no shame in deferral.
As much as you want to make progress on a certain area,
it's better to explicitly acknowledge that you can't make progress
on it--and clarify when you will be able to--then to allow the organization
to churn on an intractable problem.

### Meetings

Meetings are the final mechanism, and you can fit any and all of
the above mechanisms into a meeting. They are a universal mechanism,
although frequently overused because they can do an adequate job
of operating almost any policy.

The most common mechanism is a reporting meeting,
such as reporting progress in the Executive Weekly Meeting
as [suggested in the LLM adoption strategy](https://craftingengstrategy.com/llm-adoption-strategy/):

> **Develop an LLM-backed process for reactivating departed and suspended drivers in mature markets.**
> Through modeling our driver lifecycle, we determined that improving onboarding time will have little impact on the total number of active drivers.
> Instead, we are focusing on mechanisms to reactivate departed and suspended drivers, which is the only opportunity to meaningfully impact active drivers.
> 
> Report on progress monthly in Exec Weekly Meeting, coordinated in #exec-weekly

The other common meeting archetype is the [weekly working meeting](https://craftingengstrategy.com/strategy-testing/)
introduced in the chapter on strategy testing. Meetings are almost always the
most expensive mechanism you can find to solve a problem,
but they are easy to suggest, run, and iterate on.

If you can't find any other mechanism you believe in,
then a meeting is a decent starting point.
Just don't get too fond of them, and try to iterate
your way to canceling every meeting that you start.

## Anti-patterns

In addition to the effective operational methods discussed above,
there are a number of additional mechanisms that are frequently
used, but which I consider anti-patterns.
They can provide some value, but there's almost always a better alternative.

1. **Top-down pronouncements**:
    Sometimes a policy will be operationalized by simply declaring it must be followed.
    It's common to see a leader declare that a policy is now in effect,
    assuming that the announcement is a useful way to implement the new policy.

    For example, some "return to office" policies dictate that the team
    must work from their office, but driving a real change requires
    motivating those individuals to actually return.
2. **Education-as-announcements rollouts**: 
    The default way that many companies roll out policies is through one-time "education,"
    often as an all-company announcement for existing employees.
    They might follow up by updating training for onboarding new-hires.
    Education sounds great, but 
    a couple of trainings will never change organizational behavior.
    
    Changing behavior requires ongoing reminders, visible role models,
    inspection to understand why some teams are _not_ adopting the behavior,
    and so on. Education can be a good component of operationalizing a policy,
    but it cannot stand on its own.
3. **Mandatory recurring trainings:**
    These are a staple of compliance driven policies,
    generally because of laws which require providing a certain number
    of hours of relevant training each year.
    
    There are two deep challenges with mandatory trainings.
    First, because attendance is _required_, people tend to make little effort
    to make the content good.
    Second, many folks don't pay attention because they expect the content
    to be low quality.
    It's not uncommon to hear people say that they've never heard of a policy that
    they've performed annual training on for multiple years.
    
    It's possible to overcome these barriers, but in a situation where you're
    accountable for changing outcomes, as opposed to shifting legal obligations away from the company,
    these tend to work poorly.
4. **Just change the culture.**
    Some leaders frame most problems as cultural problems, which is a reasonable frame: most things can be usefully viewed as a cultural problem.
    Unfortunately, it's common for those who rely heavily on the cultural frame to also have a simplistic view about
    how culture is changed.

    Changing an organization's culture is tricky, and requires a combination of many
    techniques to create visible leaders role modeling the new behavior,
    and reinforcement mechanisms to ensure pockets of dissent are weeded out.
    Anyone who frames culture change as a simple or instant change is
    living in an imaginary world.
    

If you're using one of these approaches, it isn't
necessarily a bad choice. Instead, you should just make sure you can
explain why you're using it, and then you need to also make sure you
believe that explanation. If you don't, look for a mechanism from the
earlier

## What if you're not an executive?

It's easy to get discouraged when you think about which operational mechanisms
are available to you as a non-executive. So many of the frequently seen mechanisms
like running mandatory recurring meetings, or a binding architecture review process
are not accessible to you.

That is true: they're not accessible to you.
However, there's always a related mechanism that
can be implemented with less authority.
The binding architecture process can be replaced with an architectural advice process.
The mandatory review of pull requests can be replaced with a nudge.

Although it may be more common to see the authoritative mechanisms in the companies
you work in, my experience working as an executive is that these authoritative mechanisms
don't work particularly well. They do a great job of technically shifting accountability
to the wider organization, but they often don't change behavior at all.
So, instead of getting frustrated by what you can't do, focus instead on the mechanisms
that are available to you today. Add nudges, focus on the real dynamics of how colleagues
do work in your organization, and build a real dataset.

It's very hard to get an executive to support your initiative before the mechanisms
and data exist to support it, and very easy to get their support once they do.
Once you've done what you can without authority to build confidence,
if you really do need more authority,
then you're in a good place to escalate to get an executive to support your policies.

## Beware cargo-culting

The longer that I am in the industry, the more I am surprised
by how few strategists seem to care if their approach actually works.
Instead, they seem focused on doing something that _might_ work, offloading
accountability to either the organization or some team, and then moving off to
the next problem.

Perhaps this is driven by an unfortunate reality that leaders are often evaluated
by how they appear, rather than by what they accomplish.
Whether or not that's the underlying reason for why it happens,
it does make it surprisingly difficult to know which patterns to borrow
from strategy rollouts and implementations.

The best advice, unfortunately, is to remain skeptically optimistic.
Collect ideas widely, but force the ideas to prove their merit.

## Summary

Now that you've finished this chapter,
you're significantly more qualified to
write a complete, useful strategy than I was a decade into my career.
Often skipped, the operations behind your strategy are at least as
essential as any other step, and any strategy without them will fade quietly into
your organization's history.

In addition to being able to rollout a strategy of your own,
this chapter also provides a useful rescue toolkit you can use
to put an existing, floundering strategy back on track.
If you don't see an opportunity to write new strategy within your
organization, then there's still probably room to flex
your operational skill.
````

## File: llm/12000_organizing-eng-strategy-docs.md
````markdown
# Making engineering strategies more readable
url: https://craftingengstrategy.com/readable-strategy

As discussed in [Components of engineering strategy](https://craftingengstrategy.com/strategy-steps/),
a complete engineering strategy has five components: explore, diagnose, refine (map & model), policy, and operation.
However, it's actually quite challenging to read a strategy document written that way.
That's an effective sequence for *creating* a strategy, but it's a challenging sequence
for those trying to quickly *read and apply* a strategy without necessarily wanting to understand
the complete thinking behind each decision.

This post covers:

* Why the order for writing a strategy is hard to read
* How to organize a strategy document for reading
* How to refactor and merge components for improved readability
* Additional tips for effective strategy documents

After reading it, you should be able to take a written strategy and
rework it into a version that's much easier for others to read.

---

*This is an exploratory, draft chapter for a book on engineering strategy that I'm brainstorming in [#eng-strategy-book](https://lethain.com/tags/eng-strategy-book/).*
*As such, some of the links go to other draft chapters, both published drafts and very early, unpublished drafts.*

## Why writing structure inhibits reading

Most software engineers learn to structure documents early in their lives as
students writing academic essays. Academic essays are focused on presenting evidence
to support a clear thesis, and generally build forward towards their conclusion.
Some business consultancies explicitly train their new hires in business writing,
such as McKinsey teaching
Barbara Minto's *[The Pyramid Principle](https://www.amazon.com/Pyramid-Principle-Logic-Writing-Thinking/dp/0273710516)*,
but that's the exception.

While academic essays want to develop an argument, professional writing is a bit different.
Professional writing typically has one of three distinct goals:

* **Refining thinking about a given approach** ("how do we select databases for our new products?") -- this is an area where the academic structure can be useful,
    because it focuses on the thinking behind the proposal rather than the proposal itself
* **Seeking approval from stakeholders or executives** ("what database have we selected for our new analytics product?") -- this is an area where the academic structure
    creates a great deal of confusion, because it focuses on the thinking rather than the specific proposal,
    but stakeholders view the specific proposal as the primary topic to review
* **Communicating a policy to your organization** ("databases allowed for new products") -- helping engineers at your company
    understand the permitted options for a given problem, and also explaining the rationale behind the decision for
    the subset who may want to understand or challenge the current policy

The ideal format for the first case is generally at odds with the other two, which is a frequent cause of
strategy documents which struggle to graduate from brainstorm to policy.
I find that most strategy writers are resistant to the idea that it's worth their time to restructure their
initial documents, so let me expand on challenges I've encountered when I've personally tried to make
progress without restructuring:

* **Too long, didn't read.** Thinking-oriented structures leave policy recommendations at the very bottom,
    but the vast majority of strategy readers are simply trying to understand that policy so they can
    apply it to their specific problem at hand. Many of those readers, in my experience a majority of them,
    will simply give up before reading the sections that answer their questions and assume that the
    document doesn't provide clear direction because finding that direction took too long.

    This is very much akin to the core lesson of Steve Krug's [Don't Make Me Think](https://www.amazon.com/Dont-Make-Think-Revisited-Usability/dp/0321965515):
    users (and readers) don't understand, they muddle through.
    Assuming readers will invest significant time to deeply understand your document is an act of hubris.
* **Approval meeting to nowhere.** There are roughly three types of approval meetings. The first, you go in and no one has any feedback.
    Maybe someone gripes that it could have been done asynchronously instead of a meeting, but your document is approved.
    The second, there are two sets of stakeholders with incompatible goals, and you need a senior decision-maker to
    mediate between them. This is a very useful meeting, because you generally can't make progress without that
    senior decision-maker breaking the tie.
    
    The third sort of meeting is when you get derailed early with questions about the research, whether you'd considered
    another option, and whether this is even relevant. You might think this is because your strategy is wrong, but
    in my experience it's usually because you failed to structure the document to present the policy upfront.
    Stakeholders might disagree with many elements of your thinking but still agree with your ultimate policy,
    but it's only useful to dig into your rationale if they actually disagree with the policy itself.
    Avoid getting stuck debating details when you agree on the overarching approach by presenting the
    policy *first*, and only digging into those details when there's disagreement.
* **Transient alignment.** Sometimes you'll see two distinct strategy documents, with the first covering
    the full thinking, and the second only including the policy and operations sections.
    This tends to work quite well initially, but over time existing members of the team depart
    and new members are hired. At some point, a new member will challenge the thinking behind
    the strategy as obviously wrong, generally because it's a different set of policies than
    they used at the previous employer. If you omit the diagnosis and exploration sections entirely,
    then they can't trace through the decision making to understand the reasoning,
    which will often cause them to leap to simplistic conclusions like the
    ever popular, "I guess the previous engineers here were just dumb."

As annoying as each of these challenges is, the solution is simple:
use the writing structure for writing, and invert that structure for reading.

## Invert structure for reading

Reiterating a point from [Components of engineering strategy](https://craftingengstrategy.com/strategy-steps/):
it's always appropriate to change the structure that you use to develop or present a strategy,
as long as you are making a deliberate, informed decision.

While I've generally found explore, diagnose, refine, policy, and operation to work well for
writing policy, I've consistently found it a poor format for presenting strategy.
Whether I'm presenting a strategy for review or rolling the strategy out to be followed by
the wider organization, I recommend an inverted structure:

* **Policy**: what does the strategy require or allow?
* **Operation**: how is the strategy enforced and carried out, how do I get exceptions for the policy?
* **Refine**: what were the load-bearing details that informed the strategy?
* **Diagnose**: what are the more generalized trends and observations that steered the thinking?
* **Explore**: what is the high-level, wide-ranging context that we brought into creating this strategy?

When seeking approval, you'll probably focus on the **Policy** section.
When rolling it out to your organization, you'll probably focus on the **Operation** section more.
In both cases, those are the critical components and you want them upfront.
Very few strategy readers want to understand the full thinking behind your strategy, instead they just
want to understand how it impacts the specific decision they are trying to answer.

The vast majority of strategy readers want the answer, not to understand the thinking behind the answer,
and these are your least motivated readers. Someone who wants to really understand the thinking will
invest time reading through the document, even if it isn't perfectly structured for them.
Someone who just wants an answer will frequently give up and make up an answer rather than reading all
the way through to where the document does in fact answer their question.

Zooming out a bit, this is a classic "lack of user empathy" problem. Folks authoring the document
are so deep in the details that they can't put themselves in the readers' mindset to think about
how overwhelming the document would be if you were simply trying to pop in, get an answer, and then pop out.
This lack of empathy also means that most strategy writers refuse to structure their documents to
support the large population of answer seekers over the tiny population of strategy authors,
but just try it a few times and I think you'll see it helps a great deal.
Even faster, go read someone else's strategy document that you aren't familiar with, and
you'll quickly appreciate how challenging it can be to identify the actual proposal
if they follow the academic structure.

## Strategy refactoring

Inverting the structure is the first step of optimizing a document
for readability, but you don't have to stop there. Often you'll
find that even the inverted strategy structure is somewhat confusing to read
for a given document. I think of this process as "strategy refactoring."

For example, [How should you adopt LLMs?](https://craftingengstrategy.com/llm-adoption-strategy/) makes two refactors
to the inverted format. First, it merges *Refine* into *Diagnose*, which keeps
the map and models closer to the specific topics that are explored.
Second, it discards the *Operation* section entirely, and includes the relevant
details with the policies they apply to in the *Policy* section.

Strategy refactoring is about discarding structure where it interferes with usability.
The strategy structure is very effective at separating concerns while reasoning through
decision making, but most readers benefit more from engaging with the full implications at once.
Once you're done thinking, refactor away the thinking tools: don't let the best tools for
one workflow mislead you into thinking they're the best for an entirely different one.

## Additional tips for effective strategy docs

In addition to the above advice, there are a handful of smaller tips
that I've found helpful for creating readable strategy documents:

* Before releasing a document widely, find someone entirely uninvolved with the
    strategy thus far and have them point out areas that are difficult to understand.
    Anyone who's been thinking about the strategy is going to gloss over areas that might
    be inscrutinable to those who are approaching it with fresh eyes.
* Every strategy document should be rolled out with an explicit commenting period where you
    invite discussion, as well as office hours where you are available to explain how to apply
    the strategy correctly. These steps help with adoption, but even more importantly they
    help you identify dissenters who disagree with the strategy such that you can follow up
    to better understand their concerns.    
* Every company should maintain its own internal engineering strategy
    template, incorporating the notes in [making readable engineering strategies](https://craftingengstrategy.com/readable-strategy/)
* Your template should include consistent metadata, particularly when it was created,
    the current approval status, and where to ask questions.
    Of these, a clear, durable place to ask questions is the most important,
    as it slows the rate that these documents rot.
* After you release your strategy, disable in-document commenting. This isn't intended to prevent further discussion,
    but rather to move the discussion outside of the document.
    Nothing creates the impression of an unapproved, unfinished strategy document
    faster than a long string of open comments. Open comments also make it difficult
    to read the strategy document, as often the reader will get distracted from reading
    the document to read the comments.

## Summary

After reading this chapter, you know how to escape the rigid structures imposed during the
creation of a strategy to create a readable document that is easier for others to both approve and apply.
Beyond initially inverting the structure for easier reading, you also understand how to refactor sections
away entirely that may have been essential for creation but interfere with understanding how to apply the strategy,
which is by far the most common task for strategy readers.

Most importantly, I hope you finish this chapter agreeing that it's worth your time to
rework your thinking-optimized draft rather than leaving it as is. The deliberate refusal
to structure documents for readers is the root cause of a surprising number of good strategies
that utterly fail to have their intended impact.
````

## File: llm/13000_bridging-theory-and-practice.md
````markdown
# Bridging theory and practice in engineering strategy.
url: https://craftingengstrategy.com/theory-and-practice

Some people I've worked with have lost hope that engineering strategy
actually exists within _any_ engineering organizations.
I imagine that they, reading through the
[steps to build engineering strategy](https://craftingengstrategy.com/strategy-steps/),
or the [strategy for resourcing Engineering-driven projects](https://craftingengstrategy.com/project-resourcing-strategy/),
are not impressed. Instead, these ideas probably come across as theoretical at best.
In less polite company, they might describe these ideas as fake constructs.

Let's talk about it! Because they're right. In fact, they're right in two different ways.
First, this book is focused on explaining how to create clean, refined, and definitive strategy documents,
where initially most real strategy artifacts look rather messy.
Second, applying these techniques in practice can require a fair amount of creativity.
It might sound easy, but it's quite difficult in practice.

This chapter will cover:

* Why strategy documents need to be clear and definitive,
    especially when strategy development has been messy
* How to iterate on strategy when there are demands for unrealistic timelines
* Using strategy as non-executives, where others might override your strategy
* Handling dynamic, quickly changing environments where diagnosis can change frequently
* Working with indecisive stakeholders who don't provide clarity on approach
* Surviving other people's bad strategy work

Alright, let's dive into the many ways that praxis doesn't quite line up with theory.

## Clear and definitive documents

As explored in [Making engineering strategies more readable](https://craftingengstrategy.com/readable-strategy/),
documents that feel intuitive to write are often fairly difficult to read. That's because thinking tends
to be a linear-ish journey from a problem to a solution. Most readers, on the other hand, usually just
want to know the solution and then move on. That's because good strategies are read for direction
(e.g. when a team wants to understand how they're supposed to solve a specific issue at hand)
far more frequently than they're read to build agreement (e.g. building stakeholder alignment
during the initial development of the strategy).

However, many organizations only produce writer-oriented strategy documents,
and may not have any reader-oriented documents at all.
If you've predominantly worked in those sorts of organizations,
then the first reader-oriented documents you encounter will seem artificial.

There are also organizations that have many reader-oriented documents,
but omit the rationale behind those documents. Those documents feel prescriptive
and heavy-handed, because the infrequent reader who _does_ want to understand
the thinking can't find it. Further, when they want to propose an alternative,
they have to do so without the rationale behind the current policies:
the absence of that context often transforms what was a collaborative problem-solving
opportunity into a political conflict.

With that in mind, I'd encourage you to see the frequent absence of these documents
as a major opportunity to drive strategy within your organization, rather than
evidence that these documents don't work. My experience is that they do.

## Doing strategy despite unrealistic timelines

The most frequent failure mode I see for strategy is when it's rushed,
and its authors accept that thinking must stop when the artificial deadline is reached.
Taking annual planning at Stripe as an example,
[Claire Hughes Johnson](https://www.amazon.com/Scaling-People-Tactics-Management-Building/dp/1953953212/)
argued that planning expands to fit any timeline, and consequently set a short planning timeline of
several weeks. Some teams accepted that as a fixed timeline and _stopped planning_ when the timeline
ended, whereas effective teams never stopped planning before or after the planning window.

When strategy work is given an artificial or unrealistic timeline,
you should deliver the best draft you can.
Afterwards, rather than being finished, you should view yourself as
[starting the refinement process](https://craftingengstrategy.com/refine/).
An open strategy secret is that many strategies never leave
the refinement phase, and continue to be tweaked throughout their
lifespan. Why should a strategy with an early deadline be any different?

Well, there is one important problem to acknowledge:
I've often found that the executive who initially provided the
unrealistic timeline intended it as a forcing function to inspire action and quick thinking.
If you have a discussion with them directly, they're usually quite open to adjusting the approach.
However, the intermediate layers of leadership between that executive and you often calcify
on a particular approach which they claim that the executive insists on precisely following.

Sometimes having the conversation with the responsible executive is quite difficult.
In that case, you do have to work with individuals taking the strategy literally and as unalterable
until either you can have the conversation or something goes wrong enough that the executive
starts paying attention again. Usually, though, you can find someone who has a communication path,
as long as you can articulate the issue clearly.

## Using strategy as non-executives

Some engineers will argue that the only valid [strategy altitude](https://craftingengstrategy.com/when-write-stratefy/)
is the highest one defined by executives, because any other strategy can be invalidated by
a new, higher altitude strategy.
They would claim that teams simply _cannot_ do strategy, because executives might invalidate it.
Some engineering executives would argue the same thing, instead claiming that they can't work on an engineering strategy
because the missing product strategy or business strategy might introduce new constraints.

I don't agree with this line of thinking at all.
To do strategy at any altitude, you have to come to terms with the certainty that
new information will show up, and you'll need to revise your strategy to deal with that.

The strategy for [controlling access to user data](https://craftingengstrategy.com/user-data-strategy/) is a good counterexample
against the premise that effective strategy requires executive support.
The lack of progress had been framed as the result of limited executive engagement on the topic,
which had led to a disengaged team. However, as we started to work on the ergonomics of the problem,
we came to realize that we could significantly reduce unnecessary access to user data without
any top-down support at all.

When it comes to using strategy, effective diagnosis trumps authority.
At least as many executives' strategies are ravaged by reality's pervasive details as are overridden by higher altitude strategies.
The only way to be certain your strategy will fail is waiting until you're certain that
no new information might show up and require it changing.

## Doing strategy in chaotic environments

[How should you adopt LLMs?](https://craftingengstrategy.com/llm-adoption-strategy/) discusses how a company should plot a path
through the rapidly evolving LLM ecosystem.
Periods of rapid technology evolution are one reason why your strategy might encounter a pocket of chaos,
but there are many others. Pockets of rapid hiring, as well as layoffs, create chaos.
The departure of load-bearing senior leaders can change a company quickly.
Slowing revenue in a company's core business can also initiate chaotic actions
in pursuit of a new business.

Strategies don't require stable environments. Instead, strategies require awareness of
the environment that they're operating in. In a stable period, a strategy might expect
to run for several years and expect relatively little deviation from the initial approach.
In a dynamic period, the strategy might know you can only protect capacity in two-week chunks
before a new critical initiative pops up.
It's possible to execute good strategy in either scenario, but it's impossible to execute good strategy
if you don't diagnose the context effectively.

## Unreliable information

Oftentimes, the way forward is very obvious if a few key decisions were made.
You know who is supposed to make those decisions, but you simply cannot get them
to decide.
My most visceral experience of this was conducting a layoff where the CEO wouldn't
define a target cost reduction or a thesis of how much various functions (e.g. engineering, marketing, sales)
should contribute to those reductions.
With those two decisions, engineering's approach would be obvious, and without that clarity
things felt impossible.

Although I was frustrated at the time,
I've since come to appreciate that missing decisions are the norm rather than the exception.
The strategy on [Navigating Private Equity ownership](https://craftingengstrategy.com/private-equity-strategy/) deals with
this problem by acknowledging a missing decision, and expressly blocking one part of its execution
on that decision being made.
Other parts of its plan, like changing how roles are backfilled, went ahead to address
the broader cost problem.

Rather than blocking on missing information, your strategy should acknowledge what's
missing and move forward where you can. Sometimes that's moving forward by taking risk,
sometimes that's delaying for clarity, but it's never accepting that you're stuck
without options other than pointing a finger.

## Surviving other people's bad strategy work

Sometimes you will be told to follow something which is described as a strategy,
but is really just a policy without any strategic thinking behind it.
This is an unavoidable element of working in organizations and happens for all sorts of reasons.
Sometimes, your organization's leader doesn't believe it's valuable to explain their thinking to others,
because they see themselves as the one important decision maker.

Other times, your leader doesn't agree with a policy they've been instructed to roll out.
Adoption of "high hype" technologies like blockchain technologies during the crypto boom
was often top-down direction from company leadership that engineering disagreed with,
but was obligated to align with. In this case, your leader is finding that it's hard
to explain a strategy that they themselves don't understand either.

This is a frustrating situation. What I've found most effective is writing a strategy of my own,
one that acknowledges the broader strategy I disagree with in its diagnosis as a static, unavoidable truth.
From there, I've been able to make practical decisions that recognize the context, even if it's not
a context I'd have selected for myself.

## Summary

I started this chapter by acknowledging that the [steps to building engineering strategy](https://craftingengstrategy.com/strategy-steps/)
are a theory of strategy, and one that can get quite messy in practice.
Now you know why strategy documents often come across as overly pristine--because they're trying to communicate clearly
about a complex topic.

You also know how to navigate the many ways reality pulls you away from perfect strategy,
such as unrealistic timelines, higher altitude strategies invalidating your own strategy work,
working in a chaotic environment, and dealing with stakeholders who refuse to align with your strategy.
Finally, we acknowledged that sometimes strategy work done by others is not what we'd consider strategy.
It's often unsupported policy with neither a diagnosis nor an approach to operating the policy.

That's all stuff you're going to run into, and it's all stuff you're going to overcome
on the path to doing good strategy work.
````

## File: llm/14000_more-refinement-techniques.md
````markdown
# Introduction to refinement tools
url: https://craftingengstrategy.com/refinement-intro

Perhaps the most important piece of the [Steps to build an engineering strategy](https://craftingengstrategy.com/strategy-steps/)
is strategy refinement. As we already worked through the [overview of strategy refinement](https://craftingengstrategy.com/refine/)
in the "Steps" section of this book, 
the goal of the "Refinement" section is to go into much greater detail about the three
core mapping techniques:
[strategy testing](https://craftingengstrategy.com/strategy-testing/),
[systems modeling](https://craftingengstrategy.com/systems-modeling/),
and [Wardley mapping](https://craftingengstrategy.com/wardley-mapping/).

As we work through them, keep in mind that there are many other techniques out there,
such as the many covered in Eben Hewitt's *[Technology Strategy Patterns](https://lethain.com/notes-on-the-technology-strategy-patterns/)*.
This section covers those that I've found most useful, and you can find breadcrumbs to
those preferred by others in the [appendix on strategy resources](https://craftingengstrategy.com/additional-resources/).

With that said, it's time to start drilling into [strategy testing](https://craftingengstrategy.com/strategy-testing/).
````

## File: llm/15000_testing-strategy.md
````markdown
# Strategy testing: avoid the waterfall strategy trap with iterative refinement.
url: https://craftingengstrategy.com/strategy-testing

If I could only popularize one idea about technical strategy, it would be that
prematurely applying pressure to a strategy's rollout prevents evaluating whether the strategy is effective.
Pressure changes behavior in profound ways, and many of those changes are intended to make you believe your
strategy is working while minimizing change to the status quo (if you're an executive)
or get your strategy repealed (if you're not an executive). Neither is particular helpful.

While some strategies are obviously wrong from the beginning, it's much more common to see reasonable strategies that
fail because they didn't get the small details right.
Premature pressure is one common cause of a more general phenomenon:
most strategies are developed in a waterfall model,
finalizing their approach before incorporating the lessons that reality teaches
when you attempt the strategy in practice.

One effective mechanism to avoid the waterfall strategy trap is explicitly testing your strategy to refine the details.
This chapter describes the mechanics of strategy testing:

* when it's important to test strategy (and when it isn't)
* how to test strategy
* when you should stop testing
* roles in strategy testing: sponsor vs guide
* metrics and meetings to run a strategy testing
* how to identify a strategy that skipped testing
* what to do when a strategy has progressed too far without testing

Let's get into the details.

---

*This is an exploratory, draft chapter for a book on engineering strategy that I'm brainstorming in [#eng-strategy-book](https://lethain.com/tags/eng-strategy-book/).*
*As such, some of the links go to other draft chapters, both published drafts and very early, unpublished drafts.*

*Many of the ideas here came together while working with [Shawna Martell](https://www.linkedin.com/in/shawnamartell/), [Dan Fike](https://www.linkedin.com/in/danfike/), [Madhuri Sarma](https://www.linkedin.com/in/madhurisarma/), and many others in Carta Engineering.*

## When to test strategy

Strategy testing is ensuring that a strategy will accomplish its intended goal at a cost that you're willing to pay.
This means it needs to happen prior to implementing a strategy, usually in a strategy's early development stages.

A few examples of when to test common strategy topics:

* Integrating a recent acquisition might focus on getting a single API integration working
    before finalizing how the overall approach goes.
* A developer productivity strategy focused on requiring typing in a Python codebase might
    start by having an experienced team member type an important module.
* A service migration might attempt migrating both a simple component (to test migration tooling)
    and a highly complex component (to test integration complexity) before moving to a broader rollout.

In every case, the two most important pieces are testing before finalizing the strategy, and testing narrowly with a focus
on the underlying mechanics of the approach.
Avoid getting caught up in solving broad problems like motivating adoption and addressing conflicting incentives.

That's not to say that you need to test every strategy. A few of the common cases where you might not want to test a strategy are:

* When you're dealing with a [permissive strategy](https://craftingengstrategy.com/when-write-stratefy/) that's very cheap to apply,
    testing is often not too important; indeed, you can consider most highly-permissive strategies as a test
    of whether it's effective to implement a similar, but less permissive, strategy in the future.
* Where testing isn't viable for some reason. For example, a hiring strategy where you shift hiring into
    certain regions isn't something you can test in most cases, it's something you might need to run for several years
    to get meaningful signal on results.
* There are also cases where you have such high conviction in a given strategy that it's not worth testing, perhaps
    because you've done something nearly identical at the same company before.
    Hubris comes before the fall, so I'm generally skeptical of this category.

That said, my experience is that you should try very hard to find a way to test every strategy.
You certainly should not try hard to convince yourself testing a strategy isn't worthwhile.
Testing is so, so much cheaper than implementing a bad strategy, that it's almost always a good investment of time and energy.

## How to test strategy

For a valuable step that's so often skipped, strategy testing is relatively straightforward.
The approach I've found effective is:

1. Identify the narrowest, deepest available slice of your strategy, and iterate on applying your strategy to that slice until you're confident the approach works well.

    For example, if you're testing a new release strategy for your Product Engineering organization,
    decide to release exactly one important release following the new approach.
2. As you iterate, identify metrics that help you verify the approach is working; note that these aren't metrics to measure adoption, instead measure impact of the change.

    For example, metrics that show the new release process reduces customer impact, or drives more top-of-funnel visitors.
3. Operate from the belief that people are well-meaning, and strategy failures are due to excess friction and poor ergonomics.

    For example, assume the release tooling is too complex if people aren't using it. (Definitely don't assume that people are too resistant to change.)
4. Keep refining until you have conviction that your strategy's details work in practice, or that the strategy needs to be approached from a new direction.

    For example, if the metrics you identified before show the new release process has significantly
    reduced customer impact of the new release.

The most important details are the things you should _not_ do.
Don't go broad where impact _feels_ higher but iteration cycles are slower.
Don't get caught up on _forcing_ adoption such that you're distracted from improving the underlying mechanics.
Finally, don't get so attached to your current approach that you can't accept that it might not be working.
Strategy testing is only valuable because many strategies don't work as intended, and it's much cheaper
to learn that early.

## Testing roles: sponsors and guides

Sometimes the strategy testing process is led by one individual who is able to sponsor the work
(a principal engineer at a smaller company, an executive, etc) and also coordinate the day-to-day work of validating
the approach (a principal engineer at a larger company, an engineering manager, a technical program manager, etc).
It's even more common for these responsibilities to split between two roles: **sponsor** and a **guide**.

The **sponsor** is responsible for:

1. serving as an escalation point to make quick decisions to avoid getting stuck in development stages
2. pushing past historical decisions and beliefs that prevent meaningful testing
3. marshalling cross organizational support
4. telling the story to stakeholders, especially the executive team to avoid getting defunded
5. preventing overloading of strategy (where people want to make the strategy solve _their_ semi-related problem)
6. setting pace to avoid stalling out
7. identifying when energy is dropping and to change the phase of strategy (from development to implementation)

The **guide** is responsible for:

1. translating the strategy into particulars where testing gets stuck
2. identifying slowdowns and blockers
3. escalating frequently to sponsor
4. tracking goals and workstreams
5. maintaining the pace set by the sponsor

In terms of filling these roles, there are a few lessons that I've learned over time.
For sponsors, what matters the most is that they're genuinely authorized by the
company to make the decision they're making, and that they care enough about the impact
that they're willing to make difficult decisions quickly. A sponsor is only meaningful
to the extent that the guide can escalate to the sponsor, who must rapidly resolve those escalations.
If they aren't available for escalations or don't resolve them quickly, they're a poor sponsor.

For guides, you need someone who can execute at pace without getting derailed by various organizational
messes, and has good, nuanced judgment relevant to the strategy being tested.
The worst guides are ideological (they reject the very feedback created by testing)
or easily derailed (you're likely testing _because_ there's friction somewhere, so
someone who can't navigate friction is going to fail by default).

## Meetings & Metrics

The only absolute requirement for the strategy testing phase is that
the sponsor, guide, and any key folks working on the strategy **must meet together every single week**.
Within that meeting, you'll iterate on which metrics capture the current areas you're trying to refine,
discuss what you've learned from prior metrics or data, and schedule one-off followups to ensure you're making progress.

The best version of this meeting is debugging heavy and presentation light.
Any week that you're not learning something that informs subsequent testing,
or making a decision that modifies approach to testing, should be viewed with some suspicion.
It might mean that you've underresourced the testing effort, or that your testing approach is too
ambitious, but it's a meaningful signal that testing is converging too slowly to maintain attention.

If all of this seems like an overly large commitment, I'd push you to consider
your [strategy altitude](https://craftingengstrategy.com/when-write-stratefy/) to adjust the volume
or permissiveness of the strategy you're working on.
If a strategy isn't worth testing, then it's either already quite good (which should be widely evident beyond its authors)
or it's probably only worth rolling out in a highly permissive format.

## Identifying strategies that skipped testing

While not all strategies _must_ be refined by a testing phase, essentially all failing strategies skip
the testing phase to move directly into implementation.
Strategies that skip testing _sound right_, but don't accomplish much.
Fully standardizing authorization and authentication across your company on one implementation _sounds right_,
but can still fail if e.g. each team is responsible for its own approach to determining the standard.

One particularly obvious pattern is something I describe as "pressure without a plan."
This is a strategy that only "sounds right" aspect but lacks concrete details.
Service migrations are particularly prone to this, perhaps due to apocryphal descriptions of
Amazon's service migration in the 2000s, which is often summarized as a top-down zero-details mandate to switch away from the monolith.

Identification comes down to understanding two things:

1. Are there numbers that show the strategy is driving the desired impact?
    For example, API requests made into the new authentication service as a percentage of all authentication requests
    is more meaningful than a spreadsheet tracking teams' commitments to move to the new service.
    
    Try to avoid proxy metrics when possible, but to instead look at the actual thing that matters.
2. If the numbers aren't moving, is there a clear mechanism debugging and solving those issues,
    and is this team actually making progress?
    For example, a team that helps with integration with the new authentication service to understand
    where limitations are preventing effective adoption, and who are shipping working code.
    
    Because the numbers aren't moving, you need to find a different source of meaningful evidence to validate that progress is happening.
    Generally, the best bet is either new software running in a meaningful environment (e.g. production for product code).
    It's also useful to talk with skeptics or failed integrations, but be cautious of debugging exclusively with skeptics.    
    They're almost always right, but often they are out-of-date, such that they're right but aren't describing
    current problems.

Unless one of these two identifications are _obviously true_, then it's very likely that you've
found a strategy that skipped testing.

## Recovering from skipped testing

Once you've recognized a strategy that skipped testing and is now struggling,
the next question is what to do about it.
[Should we decompose our monolith?](https://craftingengstrategy.com/monolith-decomposition-strategy/) looks at recovering from a failing service migration,
and is lightly based on my experience dealing with similar, stuck service migration at both Calm and Carta.
The answer to a stuck strategy is always: write a new strategy, and make sure _not_ to skip testing this time.

Typically, the first step of this new strategy is explicitly pausing the struggling strategy
while a new testing phase occurs. This is painful to do, because the folks invested in the current
strategy will be upset with you, but there's always going to be people who disagree with any change.
Long-term, the only thing that makes most people happy is a successful strategy, and anything that
delays progress towards that is a poor investment.

Sometimes it is difficult to officially pause a struggling strategy,
in which case you have to look for an indirect mechanism to implicitly pause without
acknowledging it. For example, delaying new services while you take a month to invest into improving service provisioning
might give you enough breathing room to test the missing mechanisms from your strategy,
without requiring anyone to lose face over a failing migration.
It would be nice to always be able to say these things out loud,
but managing personalities is an enduring leadership challenge;
even when you're an executive, you just have a different set of messy stakeholders.

## Summary

Testing doesn't determine whether a strategy might be good. It exposes the missing details required to translate
a directionally accurate strategy into a strategy that works.
After reading this chapter, you know how to lead that translation process as both a sponsor
and a guide. You can set up and run the necessary meetings to test a strategy, and also put together
the bank of metrics to determine if the strategy is ready to leave refinement and move to a broader rollout.
````

## File: llm/16000_strategy-systems-modeling.md
````markdown
# Using systems modeling to refine strategy.
url: https://craftingengstrategy.com/systems-modeling

While I was probably late to learn the concept
of [strategy testing](https://craftingengstrategy.com/strategy-testing/),
I might have learned about systems modeling too early in my career,
stumbling on Donella Meadows' _[Thinking in Systems: A Primer](https://www.amazon.com/Thinking-Systems-Donella-H-Meadows-ebook/dp/B005VSRFEA/)_
before I began my career in software.
Over the years, I've discovered a number of ways to misuse systems modeling,
but it remains the most effective, flexible tool I've found to debugging complex problems.

In this chapter, we'll work through:

* a two-minute primer on the basics of systems modeling, along with resources for those looking for a deeper exploration
    of the foundational topics
* when systems modeling is a useful technique, and when it's better to
    rely on other refinement techniques like Wardley mapping or strategy testing instead
* a discussion on systems modeling tooling, why there's no perfect systems modeling tool out there,
    and how I recommend picking the tool that you build proficiency with
* the steps to build a systems model for a problem you're engaging with
* how to document your learnings from a systems model to maximize the
    chance that others will pay attention to it rather than ignoring
    it due to the unfamiliarity or complexity of the tooling
* what systems modeling can't do, even if you really want to believe it can

After working through this chapter's overview of systems modeling,
you can see the approaches implemented in a number of system models created
to refine the strategies throughout this book.
The theory of systems modeling is certainly interesting, but hopefully
seeing real models in support of concrete engineering strategies will
be even more useful.

## Two-minute primer

If you want an exceptional introduction to systems thinking, there's no better place to go than
Donella Meadows' [Thinking in Systems](https://www.amazon.com/dp/1603580557).
If you want a worse, but shorter, introduction, I wrote a short [Introduction to systems thinking](https://lethain.com/systems-thinking/)
available online and in _An Elegant Puzzle_.

If you want something _even shorter_, then here's the briefest that I can manage.

![The image is a flowchart illustrating a network request handling process. 

1. **Requests**: This is the starting point where requests are initiated.
   - If successful (OK), requests proceed to the Load Balancer.
   - A failure due to DNS resolution will result in a direct path to Failed Requests.

2. **Load Balancer**: 
   - If functioning correctly (OK), it passes requests to the Server.
   - An error in the load balancer sends requests to the Failed Requests.

3. **Server**:
   - Successful processing (OK) leads to Successful Requests.
   - If there is an error, requests go to Failed Requests.

4. **Failed Requests**: Collects any requests that encounter an error.
   - If a load balancer error caused the failure, it returns to Requests for a retry (529 HTTP).

Arrows indicate the flow of requests between stages, with OK arrows in purple and error paths in gray.](https://craftingengstrategy.com/static/blog/strategy/QualityMentalModels.png)

<p class="img-desc i tc f6">Requests succeeding and failing between a user, load balancer, and server</p>

Accumulations are called _stocks_. For example, each of the boxes (`Requests`, `Server`, etc)
in the above diagram is a stock. Changes to stocks are called `flows`. Every arrow (`OK`, `Error in server`, etc)
between stocks in the diagram is a a flow.

Systems modeling is the practice of using various configurations of stocks and flows
to understand circumstances that might otherwise have surprising behavior or are too slow
to understand from measurement. 

For example, we can use the above model to explore the tradeoffs between a load balancer that does and does not cap throughput
to a load-sensitive service behind it.

![The image is a line graph titled "SuccessfulRequests." It has two axes: the x-axis labeled "Time" ranging from 0 to 50 and the y-axis labeled "SuccessfulRequests" ranging approximately from 0 to 900.

The graph displays four lines:

1. **Unbounded SuccessfulRequests (Blue Line):** 
   - Starts near zero at the beginning and remains flat around 100 throughout the time period.

2. **Unbounded FailedRequests (Orange Line):**
   - Quickly rises from near zero at the beginning to around 900, and then remains constant for the rest of the time period.

3. **Bounded SuccessfulRequests (Green Line):**
   - Starts near zero, sharply increases around time 5, and flattens around 600 for the remainder of the period.

4. **Bounded FailedRequests (Red Line):**
   - Starts near zero, rises to approximately 400 around the same time the green line increases, and then flattens.

All lines, except the blue one, show rapid changes initially before stabilizing. A legend in the top left corner identifies each line with its corresponding metric.](https://craftingengstrategy.com/static/blog/strategy/two-min-primer-chart.png)

<p class="img-desc i tc f6">Successful and errored requests in two different scenarios</p>

Without a model, you might get into a philosophical debate about how ridiculous it is that the downstream server
is load-sensitive. With the model, it's immediately obvious that it's worthwhile protecting it, even if it certainly
is concerning that it is so sensitive. This is what models do: they create a cheap way to understand reality when
fully understanding reality is cumbersome.

<div class="bg-light-gray br4 ph3 pv1">

**More systems thinking resources**

*[Thinking in Systems: A Primer](https://www.amazon.com/Thinking-Systems-Donella-H-Meadows-ebook/dp/B005VSRFEA/)* by Donella Meadows

*[Business Dynamics: Systems Thinking and Modeling for a Complex World](https://www.amazon.com/Business-Dynamics-Systems-Thinking-Modeling/dp/007238915X)* by John D. Sterman

*[An Introduction to Systems Thinking](https://www.amazon.com/Introduction-Systems-Thinking-Richmond-2004-11-15/dp/B01FGPA45Y/)* by Barry Richmond

</div>

## When is systems modeling useful?

Although [refinement](https://craftingengstrategy.com/refine/) is an important step of developing any strategy,
some refinement techniques work better for any given strategy.
Systems modeling is extremely useful in three distinct scenarios:

1. When you're unsure where leverage points might be in a complex system,
    modeling allows you to cheaply test which levers might be meaningful.
    For example, [modeling onboarding drivers in a ride-sharing app](https://craftingengstrategy.com/llm-onboarding-model/)
    showed that improving onboarding was less important than reengaging departed drivers.
2. When you have significant data to compare against,
    which allows you to focus in on the places where the real data and your model are in tensions.
    For example, I was able to [model the impact of hiring on Uber's engineering productivity](https://lethain.com/productivity-in-the-age-of-hypergrowth/),
    and then compare that with internal data.
3. When stakeholder disagreements are based in their unstated intuitions,
    models can turns those intuitions into something structured that can be debated more effectively.

In all three categories, modeling makes it possible iterate your thinking much faster than running a live process or technology experiment
with your team. I sometimes hear concerns that modeling slows things down, but this is just an issue of familiarity.
The more you practice, modeling can be faster than asking for advice from industry peers.
The models I've developed for this book took less than an hour. (With one notable exception: [modeling Large Language Models (LLMs) impacts on developer experience](https://craftingengstrategy.com/llm-adoption-model/),
which took much longer because I deliberately used an impractical tool to reveal the importance of good tooling).

Additionally, systems modeling will often expose counter-intuitive dimensions to the problem you're working on.
For example, the model I mentioned above on LLMs' impact on developer experience suggests that effective LLMs
might cause us to spend _more_ time writing and testing code (but less fixing issues discovered post-production).
This is a bit unexpected, as you might imagine they'd reduce testing time, but reducing testing time is only valuable
to the extent that issues identified in production remains--at worst--constant; if issues found in production increases,
then reduced testing time does not contribute to increased productivity.

Modeling without praxis creates unsubstantiated conviction.
However, in combination with praxis, I've encountered few other techniques that can similar accelerate learning.

That doesn't mean that it's always the ideal refinement technique.
If you already have conviction on the general approach, and want to refine the narrow details,
then [strategy testing](https://craftingengstrategy.com/strategy-testing/) is a better option.
If you're trying to understand the evolution of a wider ecosystem, then you may prefer
Wardley mapping.

## Tooling

For an idea that's quite intuitive, the tools of systems modeling are a real obstacle to wider adoption.
Perhaps a downstream consequence of many early, popular systems modeling tools being quite expensive,
the tooling ecosystems for systems modeling has remained fragmented for some time.
There also appears to be a mix of complex requirements, patent consolidation, and perceived small market size
that's discouraged a modern solution from consolidating the tooling market.

Earlier, I mentioned that system modeling is extremely quick, but that many folks find it a slow, laborious process.
Part of that is an issue of practice, but I suspect that the quality of modeling tooling is at least as big a part of the challenge.
In the [LLMs impact on developer experience model](https://craftingengstrategy.com/llm-adoption-model/), I go about the steps of building the model in an increasingly messy spreadsheet.
This was slow, challenging, and extremely brittle. Even after finishing the model, I couldn't extend it effectively to test new ideas,
and I inadvertently introduced a number of bugs into the implementation.

Going in the opposite direction, I explored using a handful of tools, such as [Sagemodeler](https://sagemodeler.concord.org/)
or [InsightMaker](https://insightmaker.com/), which seemed like a potentially simpler toolchain
than the one I typically rely on. There are so many of these introductory toolchains for systems modeling,
but I generally find that they're either constrained in their capabilities, have a fairly high learning curve,
or make it difficult to share your model with others.

In the end, I wound up back at the toolchain that I use,
which happens to be one that I wrote some years ago,[lethain/systems](https://github.com/lethain/systems).
This is far from a perfect toolchain, but I think it's a relatively effective mechanism for demonstrating
systems modeling for a few reasons:

1. quick to create models and iterate on those models
2. easy to share those models with others for inspection and their own exploration
3. relatively low surface area for bugs in your models
4. free, open-source, self-hosted toolchain that integrates well with Jupyter ecosystem
    for diagramming, modeling and so on

You should absolutely pick _any_ tool that feels right to you, and practice with it until you feel confident
quickly modeling scenarios. Afterwards, I wouldn't recommend spending too much time thinking about tools at all:
the most important thing is to build models and learn from them quickly, and almost any tool will be sufficient
to that goal with some deliberate practice.

## How to model

Learning to system model takes some practice, so we'll approach the details of learning to
model from two directions.
First, by documenting a general structure for approaching modeling,
and second by providing breadcrumbs to the models
developed in this book for deeper exploration of particular modeling ideas.

The structure to systems modeling that I find effective is:

1. **Sketch** the stocks and flows on paper or a diagramming application (e.g.
    [Excalidraw](https://excalidraw.com/), Figma, Whimsical, etc).
    Use whatever you're comfortable with.
2. **Reason** about how you would expect a potential change to shift the flows through the diagram.
    Which flows do you expect to go up, and which down, and how would that movement help you
    evaluate whether your strategy is working?
3. **Model** the stocks and flows in your spreadsheet tool of choice.
    Start by modeling the flows from left to right (e.g. the happy path flows). Once you have that fully working,
    then start modeling the right to left flows (e.g. the exception path flows).

    See the [Modeling impact of LLMs on Developer Experience](https://craftingengstrategy.com/llm-adoption-model/) model
    for a deep dive into the particulars of creating a model.
4. **Exercise** the model by experimenting with a number of different starting values
    and determining how the rates influence the model's values.
    This is essentially performing [sensitivity analysis](https://www.investopedia.com/terms/s/sensitivityanalysis.asp)
5. **Document** the work done in the above sections into a standalone writeup.
    You can then link to that writeup from strategies that benefit from a given model's insights.
    You might link to any [section of your strategy](https://craftingengstrategy.com/strategy-steps/), depending on what
    topic the particular model explores.
    I recommend decoupling models from specific strategies, as _generally_ the details of any given
    model are a distraction from understanding a strategy, and it's best to avoid that distraction unless
    a reader is surprised by the conclusion, in which case, the link out supports drilling into the details.

As always, this is the sequence of steps that I'd encourage you to follow,
and the sequence that I generally follow, but you should adapt them to solve
the particular problems at hand.
Over time, my experience is that most of these steps--excluding documentation--turn into a single
iterative process, and that I document everything after several iterations.

## Breadcrumbs for deeper exploration

Now that we've covered the overarching approach to system modeling,
here are the breadcrumbs to specific models that go deeper on particular elements:

* [Modeling driver onboarding](https://craftingengstrategy.com/llm-onboarding-model/)
    explores how the driver lifecycle at Theoretical Ride Sharing might be improved
    with LLMs,
    and introduces using the [lethain/systems](https://github.com/lethain/systems) library
    for modeling
* [Modeling impact of LLMs on Developer Experience](https://craftingengstrategy.com/llm-adoption-model/)
    looks at how LLMs might impact developer experience at Theoretical Ride Sharing,
    and demonstrates (the downsides of) modeling with a spreadsheet
* [Modeling engineering backfill strategy](https://craftingengstrategy.com/private-equity-model/)
    studies the financial consequences of various policies for how we backfill departed
    engineers in an engineering organization, and introduces further [lethain/systems](https://github.com/lethain/systems) features
* [Modeling service provisioning at Uber](https://craftingengstrategy.com/uber-strategy-model/)
    determines whether it's possible to optimize an existing service provisioning
    workflow or if it instead needs to be replaced with a self-service workflow

Beyond these models, you can find other systems models that I've written
on my blog's [systems-thinking category](https://lethain.com/tags/systems-thinking/), and there
are numerous, great examples in the materials references in the systems modeling primer
section above.

## How to document a model

Much like [documenting strategy is challenging](https://craftingengstrategy.com/readable-strategy/),
communicating with models in a professional setting is challenging.
The core problems is that there are many distinct groups of model readers.
Some will lack familiarity with the tooling you use to develop models.
Others will try to refine, or invalidate, your model by digging into the details.

I navigate those mismatches by focusing first on the audience who
is least likely to dig into the model. I still want to keep all the details
handy, ideally in the rawest form possible to allow others to manipulate the model
themselves, but it's very much my second goal when documenting a model.

From experience, I recommended this order (it's also the order used in the models
in this book, so you'll see it in practice a number of times):

* start with learning section, with charts showing what model has taught you
* sketch and explaining the stocks and flows
* reason about what the sketch itself teaches you
* explain how you developed the model, with an emphasis on any particularly complex portions
* exercise the model by testing how changing the flows and stocks leads to different outcomes

If you remember nothing else, your document should reflect the reality that
most people don't care how you built the model, and just want the insights.
Give them the insights early, and assume no one will trust your model nearly as much as you do.
Models are an input into the strategy, never a reliable sole backer for a strategy.

## What systems modeling isn't

Although I find systems modeling a uniquely powerful way to accelerate learning,
I've also encountered many practitioners who believe that their models *are* reality
rather than *reflecting* reality.
Over time, I've developed a short list of cautions to help
would-be modelers avoid overcommitting to their model's insights:

1. **When your model and reality conflict, reality is always right.**
    At Stripe, we developed [a model to guide our reliability strategy](https://lethain.com/modeling-reliability/).
    The model was intuitively quite good, but its real-world results were mixed.
    Attachment to our early model distracted us (too much time on collecting and classifying data)
    and we were slow to engage with the most important problems (maximizing impact of scarce mitigation bandwidth, and growing mitigation bandwidth).
    We’d have been more impactful if we engaged directly with what reality was teaching us rather than looking for reasons to disregard reality’s lessons.
2. **Models are immutable, but reality isn’t.**
    I once joined an organization investing tremendous energy into hiring but nonetheless struggling to hire.
    Their intuitive model pushed them to spend years investing into top of funnel optimization,
    and later steered them to improving the closing process.
    What they weren’t able to detect was that [misalignment in interviewer expectations](https://lethain.com/getting-to-yes/) was the largest hurdle in hiring.
3. **Every model omits information; some omit critical information.**
    The service migration at Uber is a great example: modeling clarified that we _had_ to adopt a more aggressive
    approach to our service migration in order to succeed. Subsequently, we did succeed at the migration,
    but the model didn't study the consequences of completing the migration, which were a very challenging development environment.
    The model captured everything my team cared about, as the team responsible for running the migration,
    but did nothing to evaluate whether the migration was a good idea overall.

In each of those situations, two things are true: the model was extremely valuable, and the model subtly led us astray.
We would have been led astray even without a model, so the key thing to remember isn't that models are inherently misleading,
instead the risk is being overly confident about your model. A powerful tool to use in tandem with judgment, not a replacement.

## Summary

Systems modeling isn't perfect.
If you've already determined your strategy and want to refine the details,
then strategy testing is probably a better choice.
If you're trying to understand the dynamics of an evolving ecosystem,
then Wardley mapping is a more appropriate tool.

However, if you have the general shape, but lack conviction on how
the pieces fit together, systems modeling is a remarkable tool.
After this chapter, you know how to select appropriate tooling,
and how to use that tooling to model your problem at hand.
Next, we'll work through systems modeling [a handful of detailed problems](https://lethain.com/tags/systems-thinking/)
to provide concrete examples of applying this technique.
````

## File: llm/17000_wardley-mapping.md
````markdown
# Refining strategy with Wardley Mapping.
url: https://craftingengstrategy.com/wardley-mapping

The first time I heard about Wardley Mapping was
from Charity Majors discussing it on Twitter.
Of the three core [strategy refinement techniques](https://craftingengstrategy.com/refine/),
this is the technique that I've personally used the least.
Despite that, I decided to include it in this book because it
highlights how many different techniques can be used for refining strategy,
and also because it's particularly effective at looking at the broader ecosystems
your organization exists in.

Where the other techniques like [systems thinking](https://craftingengstrategy.com/systems-modeling/)
and [strategy testing](https://craftingengstrategy.com/strategy-testing/) often zoom in,
Wardley mapping is remarkably effective at zooming out.

In this chapter, we'll cover:

* A ten-minute primer on Wardley mapping
* Recommendations for tools to create Wardley maps
* When Wardley maps are an ideal strategy refinement tool,
    and when they're not
* The process I use to map, as well as integrate
    a Wardley map into strategy creation
* Breadcrumbs to specific Wardley maps that provide examples
* Documenting a Wardley map in the context of a strategy writeup
* Why I limited focus on two elements of Wardley's work: doctrines and gameplay

After working through this chapter, and digging into some
of this book's examples of Wardley Maps, you'll have a good
background to start your own mapping practice.

## Ten minute primer

Wardley maps are a technique created by Simon Wardley to ensure your strategy is grounded in reality.
Or, as mapping practitioners would say, it's a tool for creating situational awareness.
If you have a few days, you  might want to start your dive into Wardley mapping
by reading Simon Wardley's book on the topic, *[Wardley Maps](https://medium.com/wardleymaps/on-being-lost-2ef5f05eb1ec)*.
If you only have ten minutes, then this section should be enough to get you up to speed
on reading Wardley maps.

Picking an example to work through,
we're going to create a Wardley map that aims to understand a knowledge base management
product, along the lines of a wiki like Confluence or Notion.

![The image is a diagram illustrating a process flow between authors and readers through different stages. 

### Axes:
- **Vertical Axis**: Describes visibility to users, ranging from "Less visible to users" at the bottom to "More visible to users" at the top.
- **Horizontal Axis**: Represents the stages of development from "Genesis," "Custom," "Product," to "Commodity."

### Flow Elements:
- **Author** and **Reader**: Represented by circular icons with user silhouettes at the top of different stages.
- **Create Content**: An action linked to the "Author," represented by a square icon.
- **Find Content**: A stage where the user engages with the content, connected with directional arrows from "Create content" and leading towards "Read content."
- **Read Content**: An action linked to the "Reader," represented by a square icon.
- **Search Index**: A component lower in visibility, connected with arrows from "Create content" and "Find content."
- **Document Editor** and **Document Reader**: Square icons positioned midway, indicating tools used in the content creation and consumption process.

### Arrows:
- Arrows indicate the directional flow between components, showing transitions such as content creation, discovery, and consumption.

### Segmentation:
- Blue dashed vertical lines segment the flow into three areas labeled “Custom,” “Product,” and “Commodity,” indicating different phases in the process.

This diagram effectively visualizes the process from](https://craftingengstrategy.com/static/blog/strategy/intro-wardley-init.png)

<p class="img-desc i tc f6">Wardley map for a knowledge base management application</p>

You need to know three foundational concepts to read a Wardley map:

1. Maps are populated with three kinds of components: users, needs, and capabilities.
    Users exist at the top, and represent a cohort of users who will use your product.
    Each kind of user has a specific set of needs, generally tasks that they need to accomplish.
    Each need requires certain capabilities required to fulfill that need.

    Any box connecting directly to a user is a need. Any box connecting to a need is a capability.
    A capability can be connected to any number of needs, but can never connect directly to a user;
    they connect to users only indirectly via a need.
2. The x-axis is divided into four segments, representing how commoditized a capability is.
    On the far left is genesis, which represents a brand-new capability that hasn't existed before.
    On the far right is commoditized, something so standard and expected that it's unremarkable,
    like turning on a switch causing electricity to flow.
    In between are custom and product, the two categories where most items fall on the map.
    Custom represents something that requires specialized expertise and operation to function,
    such as a web application that requires software engineers to build and maintain.
    Product represents something that can generally be bought.

    In this map, document reading is commoditized: it's unremarkable if your application
    allows its users to read content. On the other hand, document editing is somewhat on the
    border of product and custom. You might integrate an existing vendor for document editing
    needs, or you might build it yourself, but in either case document editing is less commoditized
    than document reading.
3. The y-axis represents visibility to the user. In this map, reading documents is something that
    is extremely visible to the user. On the other hand, users depend on something indexing new
    documents for search, but your users will generally have no visibility into the indexing process
    or even that you have a search index to begin with.
    
Although maps can get quite complex, those three concepts are generally sufficient to allow
you to decode an arbitrarily complex map.

In addition to mapping the current state, Wardley maps are also excellent at
exploring how circumstances might change over time.
To illustrate that, let's look at a second iteration of our map,
paying particular attention to the red arrows indicating capabilities
that we expect to change in the future.

![This image is a flowchart depicting a process involving authors and readers. It shows the interactions between different stages of content creation, editing, and consumption.

- **Vertical Axis (Visibility):** 
  - The left side is labeled "More visible to users."
  - The right side is labeled "Less visible to users."

- **Horizontal Axis (Development Stage):**
  - Divided into "Genesis," "Custom," "Product," and "Commodity."

- **Elements:**
  - **Author Section:**
    - Icon of a person labeled as "Author."
    - "Create content" leads to a purple square linked to "Search Index."
  - **Document Editing:**
    - Multiple arrows lead to a "Document Editor" from "Search Index" and another process labeled "Find content."
    - An orange arrow labeled "AI-enhanced Document Editing" connects to the "Document Editor."
  - **Reader Section:**
    - Icon of a person labeled as "Reader."
    - "Find content" transitions to the "Document Editor."
    - "Read content" directs to a "Document Reader."

- **Blue Dashed Lines:**
  - Two separate sections for "Author" and "Reader."

This flowchart illustrates the processes and visibility associated with content creation, document editing, and reading, highlighting the integration of AI in document editing.](https://craftingengstrategy.com/static/blog/strategy/intro-wardley-future.png)

<p class="img-desc i tc f6">AI-enhanced document editing as future state of document editing</p>

In particular, the map now indicates that the current document creation experience will be superseded
by an AI-enhanced editing process. Critically, the map also predicts that the AI-enhanced process will be more commoditized than
its current authoring experience, perhaps because the AI-enhancement will be driven by commoditized foundational
models from providers like Anthropic and OpenAI.
Building on that, the only place left in the map for meaningful differentiation is in search indexing.
Either the knowledge base company needs to accept the implication that they will increasingly be
a search company, or they need to expand the user needs they service to find a new avenue for differentiation.

Some maps will show evolution of a given capability using a "pipeline",
a box that describes a series of expected improvements in a capability over time.

![The image is a flowchart depicting a content creation and reading process, divided into four stages: Genesis, Custom, Product, and Commodity. It consists of several components representing the roles and actions of an Author and a Reader.

1. **Vertical Axis**:
   - Labeled on the left, "More visible to users" at the top and "Less visible to users" at the bottom.

2. **Horizontal Axis**:
   - Labeled at the bottom with four stages: Genesis, Custom, Product, Commodity.

3. **Components**:
   - Icons representing "Author" and "Reader" at the top, with arrows indicating their actions.
   - "Create content," "Find content," "Read content," and "Document Reader" processes are shown in purple boxes.
   - "Search Index" and "Document Editor" are also represented as purple boxes.
   - There is a red box labeled "AI-enhanced Document Editing" linked to an orange box labeled "AI-led, Human-reviewed Document Editing."

4. **Arrows and Flow**:
   - Arrows depict the flow of actions: an Author creates content, which goes into a Search Index. Readers find and read content using the Index and Document Reader.
   - The "Document Editor" connects various processes, showing its central role.
   - The AI-enhanced area highlights the integration of AI, with specific emphasis on AI-led editing being reviewed by humans.

5. **Color Coding**:
   -](https://craftingengstrategy.com/static/blog/strategy/intro-wardley-future-pipeline.png)

<p class="img-desc i tc f6">Pipeline showing evolution of document editing</p>

Now instead of simply indicating that the authoring experience may be replaced by
an AI-enhanced capability over time, we're able to express a sequence of steps.
From the starting place of a typical editing experience, the next expected step is AI-assisted
creation, and then finally we expect AI-led creation where the author only provides high-level
direction to a machine learning-powered agent.

For completeness, it's also worth mentioning that some Wardley maps will
have an overlay, which is a box to group capabilities or requirements together by some common denominator.
This happens most frequently to indicate the responsible team for various capabilities,
but it's a technique that can be used to emphasize any interesting element of a map's topology.

![The image is a diagram depicting a workflow process, divided into stages: Genesis, Custom, Product, and Commodity. It features two main user roles, "Author" and "Reader," represented by circular icons with user silhouettes. 

**Vertical Orientation:**
- The y-axis indicates visibility to users, ranging from "Less visible to users" at the bottom to "More visible to users" at the top. 

**Horizontal Orientation:**
- The x-axis represents the progression from "Genesis" to "Commodity," with dashed vertical lines separating the stages of "Custom" and "Product."

**Process Flow:**
1. **Author Stage:**
   - "Author" is above "Create content," which has an arrow pointing downward to a purple rectangular box.
   - This leads to "Search Index" governed by the "Infra Eng Team" within a yellow ellipse at the bottom of "Custom."

2. **Reader Stage:**
   - "Reader" is linked to two tasks: "Find content" and "Read content."
   - "Find content" points to the "Document Editor" managed by the "Product Eng Team" within a yellow ellipse in the "Product" section. 
   - "Read content" connects to "Document Reader," also under the "Product Eng Team," located in the "Commodity" section.

Overall, the diagram illustrates the flow and involvement of the infrastructure and product engineering teams across different stages, showing how content is created, indexed, and accessed.](https://craftingengstrategy.com/static/blog/strategy/intro-wardley-team-overlay.png)

<p class="img-desc i tc f6">Overlay showing which teams own which capabilities</p>

At this point, you have the foundation to read a Wardley map, or get started creating your own.
Maps you encounter in the wild might appear significantly more complex than these initial examples,
but they'll be composed of the same fundamental elements.

<div class="bg-light-gray br4 ph3 pv1">

**More Wardley Mapping resources**

*[The Value Flywheel Effect](https://itrevolution.com/product/the-value-flywheel-effect/)* by David Anderson

*[Wardley Maps](https://medium.com/wardleymaps/on-being-lost-2ef5f05eb1ec)* by Simon Wardley on Medium,
also [available as PDF](https://learnwardleymapping.com/book/)

[Learn Wardley Mapping](https://learnwardleymapping.com/) by Ben Mosior

[wardleymaps.com's resources](https://list.wardleymaps.com/) and [@WardleyMaps on Youtube](https://www.youtube.com/wardleymaps)

</div>

## Tools for Wardley Mapping

Systems modeling has a serious tooling problem, which often prevents would-be adopters from
developing their systems modeling practice. Fortunately, Wardley Mapping doesn't suffer from
that problem. You can simply print out a Wardley Map and draw on it by hand.
You can also use OmniGraffle, Miro, Figma or whatever diagramming tool you're already familiar with.

There are more focused tools as well, with
Ben Mosior pulling together an excellent writeup on
[Wardley Mapping Tools as of 2024](https://learnwardleymapping.com/2024/06/24/top-5-wardley-mapping-tools-for-2024/).
Of those two, I'd strongly encourage starting with [Mapkeep](https://mapkeep.com/) as a simple, free, and intuitive
tool for your initial mapping needs.

After you've gotten some practice, you may well want to move back into your most familiar diagramming tool
to make it easier to collaborate with colleagues, but initially prioritize the simplest tool you can to avoid
losing learning momentum on configuration, setup and so on.

## When are Wardley Maps useful?

All successful strategy begins with understanding the constraints and circumstances that the strategy needs to work within.
Wardley mapping labels that understanding as situational awareness,
and creating situational awareness is the foremost goal of mapping.

Situational awareness is always useful, but it's particularly essential in highly dynamic environments where the industry around you,
competitors you're selling against, or the capabilities powering your product are shifting rapidly.
In the past several decades, there have been a number of these dynamic contexts,
including the rise of web applications, the proliferation of mobile devices,
and the expansion of machine learning techniques.

When you're in those environments, it's obvious that the world is changing rapidly.
What's sometimes easy to miss is that any strategy the needs to last longer than a
year or two is built on an evolving foundation, even if things seem very stable at the time.
For example, in the early 2010s, startups like Facebook, Uber and Digg were all operating in physical
datacenters with their owned hardware. Over a five year period, having a presence in a
physical datacenter went from the default approach for startups to a relatively unconventional solution,
as cloud based infrastructure rapidly expanded.
Any strategy written in 2010 that imagined the world of hosting was static, was destined
to be invalidated.

No tool is universally effective, and that's true here as well.
While Wardley maps are extremely helpful at understanding broad change,
my experience is that they're less helpful in the details.
If you're looping to optimize your onboarding funnel, then something like
[systems modeling](https://craftingengstrategy.com/systems-modeling/)
or
[strategy testing](https://craftingengstrategy.com/strategy-testing/)
are likely going to serve you better.

## How to Wardley Map

Learning Wardley mapping is a mix of reading others' maps and writing your own.
A variety of maps for reading are collected in the following breadcrumbs section,
and I'd recommend skimming all of them.
In this section are the concrete steps I'd encourage you to follow
for creating the first map of your own:

1. **Commit to starting small and iterating.**
    Simple maps are the foundation of complex maps.
    Even the smallest Wardley map will
    have enough detail to reveal something interesting about the environment
    you're operating in.

    Conversely, by starting complex, it's easy to get caught up in all of your
    early map's imperfections. At worst, this will cause you to lose momentum in
    creating the map. At best, it will accidentally steer your attention rather
    than facilitating discovery of which details are important to focus on.
1. **List users, needs and capabilities.**
    Identify the first one or two users for your product.
    Going back to the knowledge management example from the primer,
    your two initial users might be an author
    and a reader. From there, identify those users' needs, such as authoring content,
    finding content, and providing feedback on which content is helpful.
    Finally, write down the underlying technical capabilities necessary
    to support those needs, which might range from indexing content in a search index
    to a customer support process to deal with frustrated users.

    Remember to start small!
    On your first pass, it's fine to focus on a single user.
    As you iterate on your map, bring in more users, needs and capabilities
    until the map conveys something useful.

    Tooling for this can be a piece of paper or wherever you keep notes.

2. **Establish value chains.**
    Take your list and then connect each of the components into chains.
    For example, the reader in the above knowledge base example would then
    be connected to needing to discover content. Discovering content would
    be linked to indexing in the search index. That sequence from reader
    to discovering content to search index represents one value chain.

    Convergence across chains is a good thing.
    As your chains get more comprehensive, it's expected that a given capability
    would be referenced by multiple different needs. Similarly, it's expected that
    multiple users might have a shared need.

3. **Plot value chains** on a Wardley Map.
    You can do this using any of the tools discussed in the Tools for Wardley mapping section,
    including a piece of paper.

    Because you already have the value chains created, what you're focused on in this step
    is placing each component relative to it's visibility to users (higher up is more visible to the user,
    lower down is less visible), and how mature the solutions are (leftward represents more custom solutions,
    rightward represents most commoditized solutions).
4. **Study current state** of the map.
    With the value chains plotted on your map,
    it will begin to reveal where your organization's attention should be focused,
    and what complexity you can delegate to vendors.
    Jot down any realizations you have from this topology.
5. **Predict** evolution of the map, and create a second version of your
    map that includes these changes. (Keep the previous version so you can
    better see the evolution of your thinking!)

    It can be helpful to create multiple maps that contemplate different scenarios.
    Thinking about the running knowledge base example, you might contemplate a future where AI-powered tools become
    the dominant mechanism for authors creating content.
    Then you could explore another future where such tools are regulated out of most tools,
    and imagine how that would shape your approach differently.

    Picking the timeframe for these changes will vary on the environment
    you're mapping. Always prefer a timeframe that makes it easy to believe changes will happen,
    maybe that's five years, or maybe it's 12 months.
    If you're caught up wondering whether change might take longer than a certain timeframe,
    than simply extend your timeframe to sidestep that issue.
6. **Study future state** of the map, now that you've predicted the future,
    Once again, write down any unexpected implications of this evolution,
    and how you may need to adjust your approach as a result.
7. **Share with others** for feedback.
    It's impossible for anyone to know everything, which is why the best maps tend
    to be a communal creation. That's not to suggest that you should perform every
    step in a broad community, or that your map should be the consensus of a working group.
    Instead, you should test your map against others, see what they find insightful
    and what they find artificial in the map, and include that in your map's topology.
7. **Document** what you've learned as discussed below in the section on documentation.
    You should also connect that Wardley map writeup with your overall strategy document,
    typically in the [Refine or Explore sections](https://craftingengstrategy.com/strategy-steps/).

One downside of presenting steps to do something is that the sequence
can become a fixed recipe. These are the steps that I've found most useful,
and I'd encourage you to try them if mapping is a new tool in your toolkit,
but this is far from the canonical way.
Start here, then experiment with other approaches until you find the
best approach for you and the strategies that you're working on.

## Breadcrumbs for Wardley Map examples

<div class="bg-light-gray br4 ph3 pv1">

*I'll update these examples as I continue writing more strategies for this book.*
*Until then, I admit that some of these examples are "what I have laying around" moreso than the "ideal forms of Wardley maps."*

</div>

With the foundation in place, the best way to build on Wardley mapping is writing your
own maps. The second best way is to read existing maps that others have made,
and a number of which exist within this book:

* [LLM evolution](https://craftingengstrategy.com/wardley-llm-ecosystem/) studies the evolution of the Large Language Model ecosystem,
    and how that will impact product engineering organizations attempting to validate and deploy
    new paradigms like agentic workflows and retrieval augmented generation
* [Evolution of developer experience tooling space](https://lethain.com/measuring-developer-experience-benchmarks-theory-of-improvement/)
    explores how Wardley mapping has helped me refine my understanding of how the developer experience ecosystem
    will evolve over time

In addition to the maps within this book, I also label maps that I create on my blog
using the [wardley category](https://lethain.com/tags/wardley/).

## How to document a Wardley Map

As explored in [how to create readable strategy documents](https://craftingengstrategy.com/readable-strategy/),
the default temptation is to structure documents around the creation process.
However, it's essentially always better to write in two steps:
develop a writing-optimization version that's focused on facilitating thinking, and then rework it into
a reading-optimized version that supports both readers who are, and are not, interested in the details.

The writing-optimized version is what we discussed in "How to Wardley Map" above.
For a reading-optimized version, I recommend:

1. **How things work today** shares a map of the current environment,
    explains any interesting rationales or controversies behind placements on the map,
    and highlights the most interesting parts of the map
2. **Transition to future state** starts with a second map, this one showing the
    transition from the current state to a projected future state.
    It's very reasonable to have multiple distinct maps, each of which considers
    one potential evolution, or one step of a longer evolution.
2. **Users and Value chains** are the first place you start creating a Wardley map,
    but generally the least interesting part of explaining a map's implications.
    This isn't because the value chains are unimportant, rather it's because the map
    itself tends to implicitly explain the value chain enough that you can move directly to
    focusing on the map's most interesting implications.

    In a sufficiently complex, it's very reasonable to split this into two sections,
    but generally I find it eliminates redundancy to cover users and value chains in one
    joint section rather than separately. This is a good example of the difference between
    reading and writing: splitting these two topics helps clarify thinking, but muddles reading.

This ordering may seem too brief or a bit counter-intuitive for you, as the person who has the full set of details,
but my experience is that it will be simpler to read for most readers. That's because most readers
read until they agree with the conclusion, then stop reading, and are only interested in the details if they
disagree with the conclusion.

This format is also fairly different than the format I recommend for documenting systems models.
That is because systems model diagrams exclude much of the relevant detail, showing the relationship
between stocks but not showing the magnitude of the flows. You can only fully understand a system model
by seeing both the diagram and a chart showing the model's output.
Wardley maps, on the other hand, tend to be more self-explanatory, and often can stand on their
own with relatively less written description.

## What about doctrines and gameplay?

This book's [components of strategy](https://craftingengstrategy.com/strategy-steps/)
are most heavily influenced by Richard Rumelt's approach.
Simon Wardley's approach to strategy built around Wardley Mapping could be viewed as a competing lens.
For each problem that Rumelt's system solves, there is a Wardley solution as well,
and it's worth mentioning some of the components I've not included, and why I didn't.

The two most important components I've not discussed thus far are
Wardley's ideas of [doctrine](https://learnwardleymapping.com/2020/08/17/principles-first/)
and [gameplay](https://www.wardleymaps.com/gameplay). Wardley's doctrine are universally applicable
practices like knowing your users, biasing towards data, and design for constant evolution.
Gameplay is similar to doctrine, but is context-dependent rather than universal.
Some examples of gameplay are talent raid (hiring from knowledgeable competitors), bundling (selling products together rather than separately),
and exploiting network effects.

I decided not to spend much time on doctrine and gameplay because I find them lightly specialized
on the needs of business strategy, and consequently a bit messy to apply to the sorts of problems
that this book is most interested in solving: the problems of engineering strategy.

To be explicit, I don't personally view Rumelt's approach and Wardley's approaches as competing efforts.
What's most valuable is to have a broad toolkit, and pull in the pieces of that toolkit that feel most
applicable to the problems at hand. I find Wardley Maps exceptionally valuable at enhancing exploration,
diagnosis, and refinement in some problems. In other problems, typically shorter duration or more internally-oriented,
I find the Rumelt playbook more applicable. In all problems, I find the combination more valuable than anchoring
in one camp's perspective.

## Summary

No refinement technique will let you reliably predict the future,
but Wardley mapping is very effective at helping you plot out
the various potential futures your strategy might need to operate in.
With those futures in mind, you can tune your strategy to excel in
the most likely, and to weather the less desirable.

It took me years to dive into Wardley mapping.
Once I finally did, it was simpler than I'd feared,
and now I find myself creating Wardley maps somewhat frequently.
When you're working on your next strategy that's impacted by
the ecosystem's evolution around it, try your hand at mapping,
and soon you'll [start to build your own collection of maps](https://lethain.com/tags/wardley/).
````

## File: llm/18000_intro-ds-strategy-part.md
````markdown
# Introduction to case studies
url: https://craftingengstrategy.com/strategies-intro

This book's [Introduction](https://craftingengstrategy.com/intro/) started with a commitment to grounding its approach in concrete case studies.
In this section, we're living up to that commitment by presenting ten real-world strategies I've directly worked on or observed.
These strategies take the somewhat abstract concepts we've covered thus far and materialize them into concrete ideas,
hopefully making them easier to grasp and easier for you to apply.

The first five strategies are selected to show a varied mix of [refinement techniques](https://craftingengstrategy.com/refine/)
and [operational mechanisms](https://craftingengstrategy.com/operations/).
The next five strategies are organized by the companies in which they were implemented.
If you work through these case studies and find yourself wanting more,
the [Strategy Resources Appendix](https://craftingengstrategy.com/additional-resources/) includes suggestions
for further study.
````

## File: llm/18000_more-refinement-techniques.md
````markdown
# More ways to refine engineering strategy.

**This is a work-in-progress draft!**

todo: this needs to prototype the format for "section wrapup" chapter,
    in addition to just actually finishing this section by both recapping
    and supplementing with a number of other refinement techniques not
    covered in detail in this book

conclusion [to this introduction on engineering strategy refinement](/refine/)

Techniques from Technology Strategy Patterns

Flywheels from Good to Great
````

## File: llm/19000_uber-service-migration-strategy.md
````markdown
# Uber's service migration strategy circa 2014.
url: https://craftingengstrategy.com/uber-strategy

In early 2014, I joined as an engineering manager for Uber's Infrastructure team.
We were responsible for a wide number of things, including provisioning new services.
While the overall team I led grew significantly over time,
the subset working on service provisioning never
grew beyond four engineers.

Those four engineers successfully migrated 1,000+ services onto a new, future-proofed service platform.
More importantly, they did it while absorbing the majority, although certainly not the entirety, of the migration workload
onto that small team rather than spreading it across the 2,000+ engineers working at Uber at the time.
Their strategy serves as an interesting case study of how a team can drive strategy, even without any executive sponsor,
by focusing on solving a pressing user problem, and providing effective ergonomics while doing so.

## Reading this document

To apply this strategy, start at the top with _Policy_. To understand the thinking behind this strategy, read sections in reverse order, starting with _Explore_, then _Diagnose_ and so on.
Relative to the default structure, this document makes one tweak, folding the _Operation_ section in with  _Policy_.

More detail on this structure in [Making a readable Engineering Strategy document](https://lethain.com/readable-engineering-strategy-documents).

## Policy & Operation

We've adopted these guiding principles for
extending Uber's service platform:

* **Constrain manual provisioning allocation to maximize investment in self-service provisioning.**
    The service provisioning team will maintain a fixed allocation of one full time engineer on manual service provisioning tasks.
    We will move the remaining engineers to work on automation to speed up future service provisioning.
    This will degrade manual provisioning in the short term, but the alternative is
    permanently degrading provisioning by the influx of new service requests from newly hired product engineers.
* **Self-service must be safely usable by a new hire without Uber context.**
    It is possible today to make a Puppet or Clusto change while provisioning a new service that
    negatively impacts the production environment. This must not be true in any self-service solution.
* **Move to structured requests, and out of tickets.**
    Missing or incorrect information in provisioning requests create significant delays in provisioning.
    Further, collecting this information is the first step of moving to a self-service process.
    As such, we can get paid twice by reducing errors in manual provisioning while also
    creating the interface for self-service workflows.
* **Prefer initializing new services with good defaults rather than requiring user input.**
    Most new services are provisioned for new projects with strong timeline pressure
    but little certainty on their long-term requirements.
    These users cannot accurately predict their future needs, and expecting them to do so
    creates significant friction.

    Instead, the provisioning framework should suggest good defaults,
    and make it easy to change the settings later when users have more clarity.
    The gate from development environment to production environment is a particularly
    effective one for ensuring settings are refreshed.

We are materializing those principles into this
sequenced set of tasks:

1. Create an internal tool that coordinates service provisioning,
    replacing the process where teams request new services via Phabricator tickets.
    This new tool will maintain a schema of required fields that must be supplied,
    with the aim of eliminating the majority of back and forth between teams during service provisioning.

    In addition to capturing necessary data, this will also serve as our interface
    for automating various steps in provisioning without requiring future changes in
    the workflow to request service provisioning.
2. Extend the internal tool to generate Puppet scaffolding for new services,
    reducing the potential for errors in two ways. First, the data supplied in the service provisioning
    request can be directly included in the rendered template.
    Second, this will eliminate most human tweaking of templates where typos can create issues.
3. Port allocation poses a particularly high-risk, as reusing a port can
    break routing to an existing production service.
    As such, this will be the first area we fully automate, with the provisioning service
    supplying the allocated port rather than requiring requesting teams to provide an already allocated port.

    Doing this will require moving the port registry out of a Phabricator wiki page
    and into a database, which will allow us to guard access with a variety of checks.
4. Manual assignment of new services to servers often leads to new services being allocated
    to already heavily utilized servers. We will replace the manual assignment with an automated system, and do so
    with the intention of migrating to the Mesos/Aurora cluster once it is available for production workloads.

Each week, we'll review the size of the service provisioning queue,
along with the service provisioning time to assess whether the
strategy is working or needs to be revised.

<div class="bg-light-gray br4 ph3 pv1">

**Prolonged strategy testing**

Although I didn't have a name for this practice
in 2014 when we created and implemented this strategy,
the preceding section captures an important reality of team-led bottom-up strategy:
when you don't have authority to mandate compliance, you have to get the details right.
The best way to do that is a prolonged [strategy testing](https://craftingengstrategy.com/strategy-testing/) phase.
Indeed, because compliance is rooted in effectiveness,
my experience is that non-executive strategy development can never stop refining their approach.

</div>

## Refine

In order to refine our diagnosis, we've [created a systems model for service onboarding](https://craftingengstrategy.com/uber-strategy-model/).
This will allow us to simulate a variety of different approaches to our problem,
and determine which approach, or combination of approaches, will be most effective.

![The image is a flowchart illustrating a service provisioning process with several steps and potential failure points. Here’s a detailed description:

1. **Flowchart Structure:**
   - The flowchart consists of rectangular nodes connected by lines, with some nodes having annotations in red indicating issues.

2. **Nodes and Flow:**
   - The process starts with "requested services."
   - An arrow leads from "requested services" to "in-flight provisioning services."
   - From "in-flight provisioning services," the flow splits into two paths:
     - One leads to "unique port and name assigned."
     - Another arrow returns, marked as "Missing/incorrect info," indicating an error leading back from "unique port and name assigned" to "in-flight provisioning services."
   - Arrows from "in-flight provisioning services" and "unique port and name assigned" lead to "Puppet configuration generated."
   - A note in red, "Missing/incorrect info," points back from "Puppet configuration generated" to "in-flight provisioning services," indicating another potential issue.
   - From "Puppet configuration generated," the process flows to "Puppet configuration tested & merged."
   - A red arrow labeled "Puppet error" loops back from "Puppet configuration tested & merged" to "Puppet configuration generated."
   - The process then moves to "Server capacity allocated to service in Clusto."

3. **Additional Elements:**
   - There is a vertical dotted line connecting "product engineers](https://craftingengstrategy.com/static/blog/strategy/uber-provis-model-errors.png)

<p class="img-desc i tc f6">Systems model of provisioning services at Uber circa 2014</p>

As we exercised the model, it became clear that:

1. we are increasingly falling behind,
2. hiring onto the service provisioning team is not a viable solution, and
3. moving to a self-service approach is our only option.

While the model writeup justifies each of those statements in more detail,
we'll include two charts here. The first chart shows the status quo,
where new service provisioning requests, labeled as `Initial RequestedServices`,  quickly accumulate into a backlog.

![The image is a line graph titled "Service Provisioning Pipeline." It has two axes: the x-axis represents "Rounds" ranging from 0 to 100, and the y-axis represents the "Size of Stock," ranging from 0 to 14,000.

There are four lines on the graph, each representing different categories:

1. **Blue Line**: "Initial RequestedServices" showing a steep upward trend, increasing significantly as the rounds progress.
2. **Orange Line**: "Initial ProductEngineers" showing a slight upward trend but relatively flat compared to the blue line.
3. **Green Line**: "Initial InflightServices" maintaining a nearly constant value with a very slight increase across the rounds.
4. **Red Line**: "Initial ServerCapacityAllocated" also showing a slight upward trend, similar to the green line, but slightly above it.

A legend on the graph's top left corner identifies each line by color and name. The overall graph displays how different components in a service provisioning pipeline change over a series of rounds.](https://craftingengstrategy.com/static/blog/strategy/uber-model-diag-1.png)

<p class="img-desc i tc f6">Service provisioning model without error states</p>

Second, we have a chart comparing the outcomes between the current status quo and a self-service approach.

![The image is a line graph titled "Service Provisioning Pipeline." It displays data over 100 rounds on the x-axis and the size of stock on the y-axis, ranging from 0 to 14,000. There are four lines representing different data sets:

1. **Blue Line (Initial RequestedServices)**: Starts near the origin and increases markedly, showing a significant upward curve as it moves toward the right, reaching a peak near 14,000.

2. **Orange Line (Initial ServerCapacityAllocated)**: Begins low and shows a gradual increase, maintaining a relatively flat trajectory compared to the blue line.

3. **Green Line (SelfService RequestedServices)**: Starts close to the x-axis, showing a slight increase, staying lower and relatively constant compared to the other lines.

4. **Red Line (SelfService ServerCapacityAllocated)**: Begins near the origin and follows an upward trajectory similar to the blue line but reaches a peak close to 12,000.

The legend is located in the upper-left corner. Overall, the graph illustrates two service provisioning scenarios with contrasting growth patterns in requested services and server capacity allocation.](https://craftingengstrategy.com/static/blog/strategy/uber-model-chart-self-service.png)

<p class="img-desc i tc f6">Impact of self-service provisioning on provisioning rate</p>

In that chart, you can see that the service provisioning backlog in the self-service model remains steady,
as represented by the `SelfService RequestedServices` line. Of the various attempts to find a solution,
none of the others showed promise, including eliminating all errors in provisioning and increasing the team's
capacity by 500%.

## Diagnose

We've diagnosed the current state of service provisioning at Uber as:

* Many product engineering teams are aiming to leave the centralized monolith,
    which is generating two to three service provisioning requests each week.
    We expect this rate to increase roughly linearly with the size of the product engineering
    organization.

    Even if we disagree with this shift to additional services,
    there's no team responsible for maintaining the extensibility of the monolith,
    and working in the monolith is the number one source of developer frustration,
    so we don't have a practical counter proposal to offer engineers other than
    provisioning a new service.
* The engineering organization is doubling every six months.
    Consequently, a year from now, we expect eight to twelve service provisioning requests every week.
* Within infrastructure engineering, there is a team of four engineers responsible for service provisioning today.
    While our organization is growing at a similar rate as product engineering,
    none of that additional headcount is being allocated directly to the team working on service provisioning.
    We do not anticipate this changing.

    Some additional headcount is being allocated to Service Reliability Engineers (SREs) who
    can take on the most nuanced, complicated service provisioning work.
    However, their bandwidth is already heavily constrained across many tasks,
    so relying on SREs is an insufficient solution.
* The queue for service provisioning is already increasing in size as things are today.
    Barring some change, many services will not be provisioned in a timely fashion.
* Today, provisioning a new service takes about a week, with numerous round trips
    between the requesting team and the provisioning team.
    Missing and incorrect information between teams is the largest source of
    delay in provisioning services.

    If the provisioning team has all the necessary information and it's accurate,
    then a new service can be provisioned in about three to four hours of work across
    configuration in Puppet, metadata in Clusto, allocating ports, assigning the service to servers, and so on.
* There are few safeguards on port allocation, server assignment and so on.
    It is easy to inadvertently cause a production outage during service provisioning
    unless done with attention to detail.
    
    Given our rate of hiring, training the engineering organization to use this unsafe toolchain
    is an impractical solution: even if we train the entire organization perfectly today,
    there will be just as many untrained individuals in six months.
    Further, product engineering leadership has no interest in their team
    being diverted to service provisioning training.
* It's widely agreed across the infrastructure engineering team that
    essentially every component of service provisioning should be replaced as soon as possible,
    but there is no concrete plan to replace any of the core components.
    Further, there is no team accountable for replacing these components,
    which means the service provisioning team will either need to
    work around the current tooling or replace that tooling ourselves.
* It's urgent to unblock development of new services, but moving those new services
    to production is rarely urgent, and occurs after a long internal development period.
    Evidence of this is that requests to provision a new service generally come with significant urgency
    and internal escalations to management. After the service is provisioned for development,
    there are relatively few urgent escalations other than one-off requests for increased
    production capacity during incidents.
* Another team within infrastructure is actively exploring adoption of Mesos and Aurora,
    but there's no concrete timeline for when this might be available for our usage.
    Until they commit to supporting our workloads, we'll need to find an alternative
    solution.

## Explore

Uber's server and service infrastructure today is composed of a handful of pieces.
First, we run servers on-prem within a handful of colocations.
Second, we describe each server in Puppet manifests to support repeatable provisioning of servers.
Finally, we manage fleet and server metadata in a tool named Clusto, originally created by Digg,
which allows us to populate Puppet manifests with server and cluster appropriate metadata during provisioning.
In general, we agree that our current infrastructure is nearing its end of lifespan,
but it's less obvious what the appropriate replacements are for each piece.

There's significant internal opposition to running in the cloud,
up to and including our CEO, so we don't believe that will change
in the foreseeable future. We do however believe there's opportunity to
change our service definitions from Puppet to something along the lines of Docker,
and to change our metadata mechanism towards a more purpose-built solution
like Mesos/Aurora or Kubernetes.

As a starting point, we find it valuable to read
[Large-scale cluster management at Google with Borg](https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/43438.pdf)
which informed some elements of the approach to Kubernetes,
and
[Mesos: A Platform for Fine-Grained Resource Sharing in the Data Center](https://people.eecs.berkeley.edu/~alig/papers/mesos.pdf)
which describes the Mesos/Aurora approach.

<div class="bg-light-gray br4 ph3 pv1">

If you're wondering why there's no mention of
[Borg, Omega, and Kubernetes](https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/44843.pdf),
it's because it wasn't published until 2016, a year after this strategy was developed.

</div>

Within Uber, we have a number of ex-Twitter engineers who can speak with confidence to their experience
operating with Mesos/Aurora at Twitter. We have been unable to find anyone to speak with that has
production Kubernetes experience operating a comparably large fleet of 10,000+ servers, although
presumably someone is operating--or close to operating--Kubernetes at that scale.

Our general belief of the evolution of the ecosystem at the time
is [described in this Wardley mapping exercise on service orchestration (2014)](https://craftingengstrategy.com/uber-strategy-wardley/).

![The image is a Wardley Map, which is a strategic visualization tool that helps understand the landscape in which an organization operates.

Here's a detailed description:

1. **Axes:**
   - The **vertical axis** is labeled "Value Chain," ranging from "Invisible" at the bottom to "Visible" at the top.
   - The **horizontal axis** is labeled "Evolution," ranging from "Genesis" on the left to "Industrialized" on the right. It includes stages like "Custom," "Product (+rental)," and "Commodity (+utility)."

2. **Components:**
   - There are multiple components depicted as circles, each representing different elements or actors in the value chain. Some are connected by lines indicating their relationships or dependencies.
   - Components include:
     - **Product Engineer**: Visible and uncharted, responsible for provisioning new services.
     - **Service Provisioning Team**: Involved in routing traffic to services and adding capacity.
     - **Server Operations Team**: Manages adding server capacity to a cluster.
     - **Server Vendor** and **Datacenter Contract**: Represent more industrialized components in server provision.
     - **Service provision request workflow** and **Service orchestration pipeline**: Central components in the provisioning process.

3. **Technologies:**
   - The map specifies technologies such as **Puppet & Clusto On-prem, Mesos/Aurora On-prem, Mesos/Aurora (or Kubernetes) in cloud](https://craftingengstrategy.com/static/blog/strategy/wardley-compute-v2.png)

<p class="img-desc i tc f6">Wardley map of service orchestration</p>

One of the unknowns today is how the evolution of Mesos/Aurora and Kubernetes will look in the future.
Kubernetes seems promising with Google's backing, but there are few if any meaningful production deployments today.
Mesos/Aurora has more community support and more production deployments, but the absolute number of deployments
remains quite small, and there is no large-scale industry backer outside of Twitter.

Even further out, there's considerable excitement around "serverless" frameworks,
which seem like a likely future evolution, but canvassing the industry and our networks
we've been unable to find enough real-world usage to make an active push towards
this destination today.

<div class="bg-light-gray br4 ph3 pv1">

[Wardley mapping](https://craftingengstrategy.com/wardley-mapping/) is introduced as one of the techniques
for [strategy refinement](https://craftingengstrategy.com/refine/), but it can also be a useful
technique for exploring an dynamic ecosystem like service orchestration in 2014.

Assembling each strategy requires exercising judgment on how to compile the pieces
together most usefully, and in this case I found that the map fits most naturally
with the rest of exploration rather than in the more operationally-focused refinement
section.

</div>
````

## File: llm/20000_uber-service-systems-model.md
````markdown
# Service onboarding model for Uber (2014).
url: https://craftingengstrategy.com/uber-strategy-model

At the core of
[Uber's service migration strategy (2014)](https://craftingengstrategy.com/uber-strategy/)
is understanding the service onboarding process, and identifying the levers
to speed up that process. Here we'll develop a
[system model](https://craftingengstrategy.com/systems-modeling/)
representing that onboarding process, and exercise the model to test a number
of hypotheses about how to best speed up provisioning.

In this chapter, we'll cover:

1. Where the model of service onboarding suggested we focus on efforts
2. Developing a system model using the [lethain/systems](https://github.com/lethain/systems) package on Github.
    That model [is available in the lethain/eng-strategy-models](https://github.com/lethain/eng-strategy-models/blob/main/UberServiceOnboarding.ipynb)
    repository
3. Exercising that model to learn from it

Let's figure out what this model can teach us.

## Learnings

Even if we model this problem with a 100% success rate (e.g. no errors at all),
the backlog of requested new services continues to increase over time.
This clarifies that the problem to be solved is not the service provisioning team's efficiency
in running their current process,
but rather that the fundamental approach is not working.

![The image is a line graph titled "Service Provisioning Pipeline." It displays data over "Rounds" on the x-axis, ranging from 0 to 100, and "Size of Stock" on the y-axis, ranging from 0 to 14,000.

There are four lines, each representing different metrics:

1. **Blue Line (Initial RequestedServices):** This line starts at zero and increases steeply, displaying an exponential growth pattern.
   
2. **Orange Line (Initial ProductEngineers):** This line starts at around 2000 and shows a slight upward slope, suggesting gradual growth.

3. **Green Line (Initial InflightServices):** This line begins around 1000 and remains nearly flat, indicating very little change.

4. **Red Line (Initial ServerCapacityAllocated):** Starting around 1000, this line also remains flat with minimal increase.

A legend in the top left corner identifies which color corresponds to each metric.](https://craftingengstrategy.com/static/blog/strategy/uber-model-diag-1.png)

<p class="img-desc i tc f6">Service provisioning model without error states</p>

Although hiring is tempting as a solution, our model suggests it is not a particularly valuable approach in this scenario.
Even increasing the Service Provisioning team's staff allocated to manually provisioning services by 500%
doesn't solve the backlog of incoming requests.

![The image is a line graph titled "Service Provisioning Pipeline." It displays four lines representing different metrics over multiple rounds, ranging from 0 to 100 on the x-axis. The y-axis shows the "Size of Stock," with values ranging from 0 to 14,000.

1. **Blue Line**: Represents "Initial Requested Services." It shows a steep upward trend, starting from nearly 0 and rising to about 14,000 by round 100.

2. **Orange Line**: Represents "Initial Server Capacity Allocated." It follows a gradual upward trend, staying below 2,000 across all rounds.

3. **Green Line**: Represents "MoreInfraEng Requested Services." This line also trends upward steeply, starting near 0 and reaching around 12,000 by round 100. It runs parallel to the blue line but is slightly lower overall.

4. **Red Line**: Represents "MoreInfraEng Server Capacity Allocated." It shows a moderate upward trend, reaching just below 4,000 by round 100.

The graph illustrates changes in requested services and server capacity allocation over several rounds, comparing both "Initial" and "MoreInfraEng" scenarios.](https://craftingengstrategy.com/static/blog/strategy/uber-model-chart-infra-hiring.png)

<p class="img-desc i tc f6">Impact of infrastructure engineering hiring on service provisioning</p>

If reducing errors doesn't solve the problem, and increased hiring for the team doesn't solve the problem,
then we have to find a way to eliminate manual service provisioning entirely.
The most promising candidate is moving to a self-service provisioning model,
which our model shows solves the backlog problem effectively.

![The image is a line graph titled "Service Provisioning Pipeline." It compares four different metrics over 100 rounds on the x-axis. The y-axis represents the "Size of Stock" ranging from 0 to 14,000. There are four lines on the graph:

1. **Blue Line**: "Initial RequestedServices" - starts around 0 and increases sharply, reaching around 14,000 by round 100.
2. **Orange Line**: "Initial ServerCapacityAllocated" - remains mostly flat, slightly increasing, and stays low on the chart.
3. **Green Line**: "SelfService RequestedServices" - starts near the bottom and increases very slightly, staying low throughout.
4. **Red Line**: "SelfService ServerCapacityAllocated" - starts low and increases steadily, reaching about 12,000 by round 100.

Overall, the graph shows a significant increase in requested services for both initial and self-service categories, with differences in the allocation of server capacity.](https://craftingengstrategy.com/static/blog/strategy/uber-model-chart-self-service.png)

<p class="img-desc i tc f6">Impact of self-service provisioning on provisioning rate</p>

Refining our earlier statement, additional hiring may benefit the team if we are able to focus those
hires on building self-service provisioning, and we're able to
[ramp their productivity](https://lethain.com/productivity-in-the-age-of-hypergrowth/)
faster than the increase of incoming service provisioning requests.

## Sketch

Our initial sketch of service provisioning is a simple pipeline starting with
`requested services` and moving step by step through to `server capacity allocated`.
Some of these steps are likely much slower than others, but it gives a sense of the
stages and where things might go wrong. It also gives us a sense of what we can measure
to evaluate if our approach to provisioning is working well.

![The image is a flowchart illustrating a process related to provisioning services. It includes several rectangular boxes connected by arrows, depicting the sequence of steps:

1. **Requested Services**: At the start, this box is linked to "in-flight provisioning services" by a solid arrow.

2. **In-flight Provisioning Services**: This leads to "unique port and name assigned" with a rightward arrow.

3. **Unique Port and Name Assigned**: From this point, three rightward arrows guide to subsequent steps:
   - **Puppet Configuration Generated**: This is where the configuration for a service is created.
   - **Puppet Configuration Tested & Merged**: The configuration undergoes testing and merging.
   - **Server Capacity Allocated to Service in Clusto**: Finally, the server capacity is allocated for the service.

To the left of these central steps are vertically aligned boxes:
- **Product Engineers**: Dotted lines indicate influence or association with "requested services."
- **Hiring Rate**: Similarly, connected to "product engineers." 

The layout suggests coordination between service requests, configuration processes, and resource allocation.](https://craftingengstrategy.com/static/blog/strategy/uber-provis-model.png)

<p class="img-desc i tc f6">Systems model of provisioning services</p>

One element worth mentioning is the dotted lines from `hiring rate` to `product engineers` and
from `product engineers` to `requested services`. These are called _links_, which are stocks that
influence another stock, but don't flow directly into them.

<div class="bg-light-gray br4 ph3 pv1">

A purist would correctly note that links should connect to flows rather than stocks.
That is true! However, as we'll encounter when we convert this sketch into a model,
there are actually several counterintuitive elements here that are necessary to model
this system but make the sketch less readable.
As a modeler, you'll frequently encounter these sorts of tradeoffs,
and you'll have to decide what choices serve your needs best in the moment.

</div>

The biggest missing element the initial model is error flows,
where things can sometimes go wrong in addition to sometimes going right.
There are many ways things can go wrong, but we're going to focus on modeling
three error flows in particular:

1. `Missing/incorrect information` occurs twice in this model, and throws
    a provisioning request back into the initial provisioning phase where information is collected.
    
    When this occurs during port assignment, this is a relatively small trip backwards.
    However, when it occurs in Puppet configuration, this is a significantly larger
    step backwards.
2. `Puppet error` occurs in the second to final stock, `Puppet configuration tested & merged`.
    This sends requests back one step in the provisioning flow.

Updating our sketch to reflect these flows, we get a fairly complete and somewhat nuanced,
view of the service provisioning flow.

![The image is a flowchart that outlines a process involving service provisioning and configuration. Here's a detailed breakdown:

- **Starting Point**: The process begins with "requested services," represented by a rectangular box.

- **Step 1**: The services go to "in-flight provisioning services."

- **Step 2**: A "unique port and name assigned" to each service.

- **Step 3**: "Puppet configuration generated" for the service.

- **Step 4**: This configuration is "tested & merged."

- **Step 5**: "Server capacity allocated to service in Clusto."

**Additional Elements**:

- **Connections**:
  - Flow arrows connect each step, indicating the sequence from one process to another.
  - A red arrow labeled "Missing/incorrect info" points back from "unique port and name assigned" and "Puppet configuration generated" to "in-flight provisioning services," indicating potential feedback loops for missing or incorrect information.
  - Another red arrow labeled "Puppet error" points back from "Puppet configuration generated" to "in-flight provisioning services."

- **Supporting Processes**: 
  - To the side, there is a vertical sequence of two labeled boxes: "product engineers" connected by a dotted line to "hiring rate."

The flowchart primarily illustrates the process of provisioning services and highlights where errors or missing information could cause a feedback loop in the provision and configuration.](https://craftingengstrategy.com/static/blog/strategy/uber-provis-model-errors.png)

<p class="img-desc i tc f6">Model of provisioning services with error transitions</p>

Note that the combination of these two flows introduces the possibility of a service
being almost fully provisioned, but then traveling from Puppet testing back to Puppet configuration
due to `Puppet error`, and then backwards again to the initial step due to `Missing/incorrect information`.
This means nearly all provisioning progress can be lost if things go wrong.

There are more nuances we could introduce here, but there's already enough complexity here for us
to learn quite a bit from this model.

## Reason

Studying our sketches, a few things stand out:

1. The hiring of product engineers is going to drive up service provisioning requests
    over time, but there's no counterbalancing hiring of infrastructure engineers to
    work on service provisioning. This means there's an implicit, but very real,
    deadline to scale this process independently of the size of the infrastructure
    engineering team.

    Even without building the full model, it's clear that we have to either stop hiring product engineers,
    turn this into a self-service solution, or find a new mechanism to discourage
    service provisioning.
2. The size of error rates are going to influence results a great deal,
    particularly those for `Missing/incorrect information`.
    This is probably the most valuable place to start looking for efficiency improvements.
3. Missing information errors are more expensive than the model implies,
    because they require coordination across teams to resolve.
    Conversely, Puppet testing errors are probably cheaper than the model
    implies, because they should be solvable within the same team and
    consequently benefit from a quick iteration loop.

Now we need to build a model that helps guide our inquiry into those questions.

## Model

You can find the [full implementation of this model on Github](https://github.com/lethain/eng-strategy-models/blob/main/UberServiceOnboarding.ipynb)
if you want to see the entirety rather than these emphasized snippets.

First, let's get the success states working:

    HiringRate(10)
    ProductEngineers(1000)
    [PotentialHires] > ProductEngineers @ HiringRate

    [PotentialServices] > RequestedServices(10) @ ProductEngineers / 10
    RequestedServices > InflightServices(0, 10) @ Leak(1.0)
    InflightServices > PortNameAssigned @ Leak(1.0)
    PortNameAssigned > PuppetGenerated @ Leak(1.0)
    PuppetGenerated > PuppetConfigMerged @ Leak(1.0)
    PuppetConfigMerged > ServerCapacityAllocated @ Leak(1.0)

As we run this model, we can see that the number of requested services grows significantly over
time. This makes sense, as we're only able to provision a maximum of ten services per round.

![The image is a line graph titled "Service Provisioning Pipeline." It features four distinct lines, each representing different data categories over a series of rounds (0 to 100). The x-axis represents the "Rounds," while the y-axis represents the "Size of Stock," ranging from 0 to 14,000.

1. **Blue Line - Initial RequestedServices:**
   - Shows a steep, continuous increase over the rounds.
   - Starts at 0 and reaches over 14,000 by the end.

2. **Orange Line - Initial ProductEngineers:**
   - Remains mostly flat with a slight upward trend.
   - Starts above 1,000 and ends just below 2,000.

3. **Green Line - Initial InflightServices:**
   - Remains almost flat with a very slight increase.
   - Starts and ends close to 0.

4. **Red Line - Initial ServerCapacityAllocated:**
   - Shows a slight upward trend.
   - Starts above 0 and ends above 1,000.

The legend, located near the top center, clearly identifies the color and description of each line.](https://craftingengstrategy.com/static/blog/strategy/uber-model-diag-1.png)

<p class="img-desc i tc f6">Service provisioning model without error states</p>

However, it's also the best case, because we're not capturing the three error states:

1. Unique port and name assignment can fail because of missing or incorrect information
2. Puppet configuration can also fail due to missing or incorrect information.
3. Puppet configurations can have errors in them, requiring rework.

Let's update the model to include these failure modes, starting with unique port and name assignment.
The error-free version looks like this:

    InflightServices > PortNameAssigned @ Leak(1.0)

Now let's add in an error rate, where 20% of requests are missing information
and return to inflight services stock.

    PortNameAssigned > PuppetGenerated @ Leak(0.8)
    PortNameAssigned > RequestedServices @ Leak(0.2)

Then let's do the same thing for puppet configuration errors:

    # original version
    PuppetGenerated > PuppetConfigMerged @ Leak(1.0)

    # updated version with errors
    PuppetGenerated > PuppetConfigMerged @ Leak(0.8)
    PuppetGenerated > InflightServices @ Leak(0.2)

Finally, we'll make a similar change to represent errors
made in the Puppet templates themselves:

    # original version
    PuppetConfigMerged > ServerCapacityAllocated @ Leak(1.0)

    # updated version with errors
    PuppetConfigMerged > ServerCapacityAllocated @ Leak(0.8)
    PuppetConfigMerged > PuppetGenerated @ Leak(0.2)

Even with relatively low error rates, we can see that the throughput of the system
overall has been meaningfully impacted by introducing these errors.

![This image is a line graph titled "Service Provisioning Pipeline." It displays four different data series over a range of 0 to 100 rounds on the x-axis. The y-axis represents the "Size of Stock" ranging from 0 to 1000.

- **Blue Line**: Represents "Initial InflightServices", which appears as a flat line near zero, indicating no significant change over the rounds.
  
- **Orange Line**: Represents "Initial ServerCapacityAllocated", showing a steady linear increase from 0, reaching a high point by the end of the graph.
  
- **Green Line**: Represents "Errors InflightServices", which also remains flat near zero, similar to the blue line.
  
- **Red Line**: Represents "Errors ServerCapacityAllocated", showing a steady linear increase, although at a slower rate than the orange line, over the rounds.

A legend in the top left corner identifies the lines by color and label. The chart suggests a comparison of different service and error metrics over time or iterations.](https://craftingengstrategy.com/static/blog/strategy/uber-model-diag-2.png)

<p class="img-desc i tc f6">Service provisioning model with error states</p>

Now that we have the foundation of the model built, it's time to start
exercising the model to understand the problem space a bit better.

## Exercise

We already know the errors are impacting throughput, but let's start by
narrowing down which of errors matter most by increasing the error rate
for each of them independently and comparing the impact.

To model this, we'll create three new specifications, each of which increases
one error from from 20% error rate to 50% error rate, and see how the overall
throughput of the system is affected:

    # test 1: port assignment errors increased
    PortNameAssigned > PuppetGenerated @ Leak(0.5)
    PortNameAssigned > RequestedServices @ Leak(0.5)

    # test 2: puppet generated errors increased
    PuppetGenerated > PuppetConfigMerged @ Leak(0.5)
    PuppetGenerated > InflightServices @ Leak(0.5)

    # test 3: puppet merged errors increased
    PuppetConfigMerged > ServerCapacityAllocated @ Leak(0.5)
    PuppetConfigMerged > PuppetGenerated @ Leak(0.5)

Comparing the impact of increasing the error rates from 20% to 50% in each
of the three error loops, we can get a sense of the model's sensitivity to each error.

![The image is a line graph titled "Impact of Error Rates on Provisioning Pipeline". It plots the "Size of Stock" on the y-axis against "Rounds" on the x-axis, which ranges from 0 to 100. There are three lines representing different server capacities:

1. **PortErrors ServerCapacityAllocated** (Blue Line): This line shows a steady increase with a lower slope compared to the others, indicating slower growth in stock size over the rounds.

2. **PuppetGenerated ServerCapacityAllocated** (Orange Line): This line has the steepest slope, indicating a faster rate of stock size increase compared to the others.

3. **PuppetMerged ServerCapacityAllocated** (Green Line): This line is intermediate in slope between the blue and orange lines, indicating moderate growth in stock size.

The lines diverge more as rounds increase, showing varying impacts on provisioning. The legend in the top-left corner designates the colors and labels for each line.](https://craftingengstrategy.com/static/blog/strategy/uber-model-chart-diff-errors.png)

<p class="img-desc i tc f6">Impact of error rates across stages of provisioning</p>

This chart captures why exercising is so impactful: we'd assumed during sketching that
errors in puppet generation would matter the most because they caused a long trip backwards,
but it turns out a very high error rate early in the process matters even more because
there are still multiple other potential errors later on that compound on its increase.

Next we can get a sense of the impact of hiring more people onto the service
provisioning team to manually provision more services, which we can model by
increasing the maximum size of the inflight services stock from `10` to `50`.

    # initial model
    RequestedServices > InflightServices(0, 10) @ Leak(1.0)

    # with 5x capacity!
    RequestedServices > InflightServices(0, 50) @ Leak(1.0)

Unfortunately, we can see that even increasing the team's capacity by 500% doesn't solve the backlog of requested services.

![The image is a line graph titled "Service Provisioning Pipeline." It depicts the growth of service requests and server capacity over rounds, measured on the x-axis ranging from 0 to 100. The y-axis represents the "Size of Stock" ranging from 0 to 14,000. 

There are four lines:

1. **Blue Line**: Represents "Initial RequestedServices," showing a steep upward trend starting near 0 to above 14,000.
2. **Orange Line**: Represents "Initial ServerCapacityAllocated," with a gradual increase starting near 0 and rising to just over 2,500.
3. **Green Line**: Represents "MoreInfraEng RequestedServices," showing a steeper increase than the orange line, ending below 14,000.
4. **Red Line**: Represents "MoreInfraEng ServerCapacityAllocated," mirroring the orange line but with a slightly steeper slope, ending above 3,000.

The graph shows that both requested services grow faster than server capacity, with "MoreInfraEng" having greater growth rates than the initial condition. The legend is located in the upper right corner of the graph.](https://craftingengstrategy.com/static/blog/strategy/uber-model-chart-infra-hiring.png)

<p class="img-desc i tc f6">Impact of infrastructure engineering hiring on service provisioning</p>

There's some impact, but that much, and the backlog of requested services remains extremely high.
We can conclude that more infrastructure hiring isn't the solution we need, but let's
see if moving to self-service is a plausible solution.

We can simulate the impact of moving to self-service by removing the maximum size from
inflight services entirely:

    # initial model
    RequestedServices > InflightServices(0, 10) @ Leak(1.0)

    # simulating self-service
    RequestedServices > InflightServices(0) @ Leak(1.0)

We can see this finally solves the backlog.

![The image is a line graph titled "Service Provisioning Pipeline." It shows the relationship between the number of rounds on the x-axis and the size of stock on the y-axis, which ranges from 0 to 14,000.

There are four lines representing different metrics:

1. **Blue Line:** "Initial Requested Services" - This line starts at the origin and grows steeply, indicating a rapid increase in requested services over the rounds.

2. **Orange Line:** "Initial Server Capacity Allocated" - This line starts near the origin and remains almost flat, indicating little change in allocated server capacity over the rounds.

3. **Green Line:** "SelfService Requested Services" - This line also starts near the origin and stays relatively flat, suggesting minimal change in self-service requested services.

4. **Red Line:** "SelfService Server Capacity Allocated" - This line starts near the origin and increases steadily, indicating a gradual increase in self-service server capacity allocation.

The graph suggests a comparison between initial and self-service metrics regarding requested services and server capacity allocated.](https://craftingengstrategy.com/static/blog/strategy/uber-model-chart-self-service.png)

<p class="img-desc i tc f6">Impact of self-service provisioning on provisioning rate</p>

At this point, we've exercised the model a fair amount and have a good sense of what it wants to tell us.
We know which errors matter the most to invest in early, and we also know that we need to make the
move to a self-service platform sometime soon.
````

## File: llm/21000_wardley-compute-llm.md
````markdown
# Wardley mapping the service orchestration ecosystem (2014).
url: https://craftingengstrategy.com/uber-strategy-wardley

In [Uber's 2014 service migration strategy](https://craftingengstrategy.com/uber-strategy/),
we explore how to navigate the move from a Python monolith to a services-oriented
architecture while also scaling with user traffic that doubled every six months.

This [Wardley map](https://craftingengstrategy.com/wardley-mapping/) explores how orchestration frameworks were evolving
during that period to be used as an input into determining the most effective path forward
for Uber's Infrastructure Engineering team.

## Reading this map

To quickly understand this Wardley Map, read from top to bottom.
If you want to review how this map was _written_, then you should
read section by section from the bottom up, starting with Users, then Value Chains, and so on.

More detail on this structure in [Refining strategy with Wardley Mapping](https://craftingengstrategy.com/wardley-mapping/).

## How things work today

There are three primary internal teams involved in service provisioning.
The Service Provisioning Team abstracts applications developed by Product Engineering from servers managed by the Server Operations Team.
As more servers are added to support application scaling, this is invisible to the
applications themselves, freeing Product Engineers to focus on what the company
values the most: developing more application functionality.

![The image is a Wardley Map, a strategic tool used to visualize the components of a value chain and their evolution over time. Here's a detailed description:

1. **Axes**:
   - The vertical axis is labeled "Value Chain," ranging from "Invisible" at the bottom to "Visible" at the top.
   - The horizontal axis is labeled "Evolution," ranging from "Genesis" on the left to "Commodity (+utility)" on the right, with intermediate stages labeled as "Custom" and "Product (+rental)."

2. **Components**:
   - Several nodes represent different components or activities. These include:
     - Product Engineer
     - Service Provisioning Team
     - Provision new service
     - Route traffic to service
     - Add capacity to provisioned service
     - Server Operations Team
     - Service provision request workflow
     - Cluster metadata
     - Request routing infrastructure
     - Add server capacity to cluster
     - Server
     - Server vendor
     - Datacenter Contract

3. **Connections**:
   - The nodes are connected by lines, indicating the relationships and dependencies between the components.

4. **Positioning**:
   - Components are positioned along the evolution axis to show their maturity level, from initial stages (Genesis) to more mature stages (Commodity).

5. **Patterns**:
   - The map illustrates how different components are positioned in terms of visibility and evolution, helping to identify areas of potential improvement or strategic focus](https://craftingengstrategy.com/static/blog/strategy/wardley-compute-v1.png)

<p class="img-desc i tc f6">Wardley map for service orchestration</p>

The challenges within the current value chain are cost-efficient scaling, reliable deployment,
and fast deployment. All three of those problems anchor on the same underlying problem of
resource scheduling. We want to make a significant investment into improving our resource
scheduling, and believe that understanding the industry's trend for resource scheduling
underpins making an effective choice.

## Transition to future state

Most interesting cluster orchestration problems are anchored in
cluster metadata and resource scheduling.
Request routing, whether through DNS entries or allocated ports, depends on cluster metadata.
Mapping services to a fleet of servers depends on resource scheduling managing cluster metadata.
Deployment and autoscaling both depend on cluster metadata.

![The image is a complex diagram resembling a Wardley map, which illustrates the components and interactions involved in a service provisioning system. Here’s a detailed description:

1. **Axes**:
   - The vertical axis is labeled "Value Chain," ranging from "Invisible" at the bottom to "Visible" at the top.
   - The horizontal axis is labeled "Evolution," ranging from "Genesis" on the left to "Industrialized" on the right.

2. **Main Components**:
   - **Product Engineer**: Positioned near the top in the visible section, involved in provisioning new services.
   - **Service Provisioning Team**: Positioned in the visible section, connected to several components like provisioning new services and routing traffic.
   - **Server Operations Team**: Located in the industrialized-visible section, associated with adding server capacity and provisioning services.

3. **Processes**:
   - **Provision New Service**: Linked from the product engineer to other components like service provisioning and routing traffic.
   - **Route Traffic to Service**: An important function, connected to various components and stages.
   - **Add Capacity to Provisioned Service**: Connected to several teams and functions.

4. **Infrastructure**:
   - **Puppet & Clusto On-prem**: Positioned lower in the genesis section, indicating early-stage or custom solutions.
   - **Mesos/Aurora and Kubernetes**: Visible in progression, from on-prem to cloud-based solutions.
   - **Serverless](https://craftingengstrategy.com/static/blog/strategy/wardley-compute-v2.png)

<p class="img-desc i tc f6">Pipeline showing progression of service orchestration over time</p>

This is also an area where we see significant changes occurring in 2014.

Uber initially solved this problem using Clusto, an open-source tool released by Digg
with goals similar to Hashicorp's [Consul](https://www.consul.io/)
but with limited adoption. We also used [Puppet](https://www.puppet.com/) for configuring servers, alongside custom scripting.
This has worked, but has required custom, ongoing support for scheduling.
The key question we're confronted with is whether to build our own scheduling algorithms (e.g. [bin packing](https://en.wikipedia.org/wiki/Bin_packing_problem))
or adopt a different approach.
It seems clear that the industry intends to directly solve this problem via two paths:
relying on Cloud providers for orchestration (Amazon Web Services, Google Cloud Platform, etc)
and through open-source scheduling frameworks such as Mesos and Kubernetes.

Industry peers with more than five years of infrastructure experience are almost unanimously
adopting open-source scheduling frameworks to better support their physical infrastructure.
This will give them a tool to perform a bridged migration from physical infrastructure to cloud infrastructure.

Newer companies with less existing infrastructure are moving directly to the cloud, and avoiding the orchestration problem entirely.
The only companies not adopting one of these two approaches are extraordinarily large and complex
(think Google or Microsoft) or allergic to making any technical change at all.

From this analysis, it's clear that continuing our reliance on Clusto and Puppet is going to
be an expensive investment that's not particularly aligned with the industry's evolution.

## User & Value Chains

This map focuses on the orchestration ecosystem within a single company,
with a focus on what did, and did not, stay the same from roughly
2008 to 2014. It focuses in particular on three users:

1. **Product Engineers** are focused on provisioning new services,
    and then deploying new versions of that service as they make changes.
    They are wholly focused on their own service, and entirely unaware of anything beneath the orchestration layer
    (including any servers).
2. **Service Provisioning Team**
    focuses on provisioning new services, orchestrating resources for those services,
    and routing traffic to those services.
    This team acts as the bridge between the Product Engineers and the Server Operations Team.
3. **Server Operations Team** is focused on adding server capacity to be used for orchestration.
    They work closely with the Service Provisioning Team, and have no contact with the Product Engineers.

It's worth acknowledging that, in practice, these are artificial aggregates of multiple underlying teams.
For example, routing traffic between services and servers is typically handled by a Traffic or Service Networking team.
However, these omissions are intended to clarify the distinctions relevant to the evolution of orchestration tooling.
````

## File: llm/22000_llm-adoption-strategy.md
````markdown
# How should you adopt LLMs?
url: https://craftingengstrategy.com/llm-adoption-strategy

Whether you’re a product engineer, a product manager, or an engineering executive, you’ve probably been pushed to consider using Large Language Models (LLMs) to extend your product or enhance your processes. 2023-2024 is an interesting era for LLM adoption, where these capabilities have transitioned into the mainstream, with many companies worrying that they’re falling behind despite the fact that most integrations appear superficial.

That context makes LLM adoption a great topic for a strategy case study. This document is an engineering strategy document determining how a hypothetical company, Theoretical Ride Sharing, could adopt LLMs.

Building out the scenario a bit before diving into the strategy: Theoretical has 2,000 employees, 300 of which are software engineers. They’ve raised $400m, are doing $50m in annual revenue, and are operating in 200 cities across North America and Europe.
They are a ride sharing business, similar to Uber or Lyft. However, they’ve innovated by using larger vehicles—essentially reinventing public transit.

## Reading this document

To apply this strategy, start at the top with _Policy_. To understand the thinking behind this strategy, read sections in reserve order, starting with _Explore_, then _Diagnose_ and so on.
Relative to the default structure, this document has been refactored in two ways
to improve readability:
first, _Operation_ has been folded into _Policy_;
second, _Refine_ has been embedded in _Diagnose_.

More detail on this structure in [Making a readable Engineering Strategy document](https://lethain.com/readable-engineering-strategy-documents).

## Policy

Our combined policy for using LLMs at Theoretical Ride Sharing are:

* **Develop an LLM-backed process for reactivating departed and suspended drivers in mature markets.**
    Through modeling [our driver lifecycle](https://craftingengstrategy.com/llm-onboarding-model/), we determined that improving onboarding time
    will have little impact on the total number of active drivers. Instead, we are focusing on mechanisms to reactivate
    departed and suspended drivers, which is the only opportunity to meaningfully impact active drivers.

    Report on progress monthly in _Exec Weekly Meeting_, coordinated in #exec-weekly
* **Start with Anthropic.**
    We use Anthropic models, which are available through our existing cloud provider via [AWS Bedrock](https://aws.amazon.com/bedrock/). To avoid maintaining multiple implementations, where we view the underlying foundational model quality to be somewhat undifferentiated, we are not looking to adopt a broad set of LLMs at this point.
    This is anchored in our [Wardley map of the LLM ecosystem](https://craftingengstrategy.com/wardley-llm-ecosystem/).

    Exceptions will be reviewed by the _Machine Learning Review_ in #ml-review
* **Developer experience team (DX) must offer at least one LLM-backed developer productivity tool.**
    This tool should enhance the experience, speed, or quality of writing software in TypeScript. This tool should help us develop our thinking for next year, such that we have conviction increasing (or decreasing!) our investment. This tool should be available to all engineers. Adopting one tool is the required baseline, if DX identifies further interesting tools, e.g. Github Copilot, they are empowered to bring the request to the _Engineering Exec_ team for review. Review will focus on balancing our rate of learning, vendor cost, and data security.
    We've [modeled options for measuring LLMs' impact on developer experience](https://craftingengstrategy.com/llm-adoption-model/).

    Vendor approvals to be reviewed in #cto
* **Internal Tools team (INT) must offer at least one LLM-backed ad-hoc prompting tool.**
    This tool should support arbitrary non-engineering use cases for LLMs, such as text extraction, rewriting notes, and so on. It must be usable with customer data while also honoring our existing data processing commitments. This tool should be available to all employees.

    Vendor approvals to be reviewed in #coo
* **Refresh policy in six months.**
    Our primary goal is to quickly learn about this unfamiliar domain where we have limited internal expertise,
    then review whether we should increase our investment afterwards.

    Flag questions and suggestions in #cto

## Diagnose

Here’s a summary of the challenges we face in adopting LLMs at Theoretical Ride Sharing:

1. There are, at minimum, **three distinct needs** that folks internally are asking us to solve (either separately or with a shared solution):
    1. _productivity tools for non-engineers_, e.g. ad-hoc document rewriting, document summarization
    2. _productivity tools for engineers_, e.g. advanced autocomplete tooling like Github Copilot
    3. _product extensions_, e.g. high-quality document extraction in driver onboarding workflows
2. Of the above, **we see product extensions are potential strategic differentiation**, and the other two as workflow optimizations that improve our productivity but don’t necessarily differentiate us from the broader industry. Some of the opportunities for strategic differentiation we see are:
    1. *Reactivating the departed and suspended drivers* is our largest lever to increasing active drivers,
        as explored in our [model of the driver lifecycle](https://craftingengstrategy.com/llm-onboarding-model/)
    2. *Faster driver onboarding* with less human involvement will not increase active drivers, but we see a clear opportunity for LLMs to reduce operating
        costs, which may be worthwhile even if it doesn't address the core problem of active drivers
    3. *Improved customer support* by increasing the response speed and quality of our responses to customer inquiries
3. **We currently have limited experience or expertise in using LLMs in the company and in the industry.** Prolific thought leadership to the contrary, there are very few companies or products using LLMs in scaled, differentiated ways. That’s currently true for us as well
4. **We want to develop our expertise without making an irreversible commitment.** We think that our internal expertise is a limiter for effective problem selection and utilization of LLMs, and that developing our expertise will help us become more effective in iterative future decisions on this topic. Conversely, we believe that making a major investment now, prior to developing our in-house expertise, would be relatively high risk and low reward given no other industry players appear to have identified a meaningful advantage at this point
5. **Switching across foundational models and foundational model providers is cheap**. This is true both economically (low financial commitment) and from an integration cost perspective (APIs and usage is largely consistent across providers)
6. **Foundational models and providers are evolving rapidly, and it’s unclear how the space will evolve.** It’s likely that current foundational model providers will train one or two additional generations of foundational models with larger datasets, but at some point they will become cost prohibitive to train (e.g. the next major version of OpenAI or Anthropic models seem likely to cost $500m+ to train). Differentiation might move into developer-experience at that point. Open source models like LLaMa might become significantly cost-advantaged. Or something else entirely. The future is wide open.

    We've built a Wardley map to understand the [possible evolution of the foundational model ecosystem](https://craftingengstrategy.com/wardley-llm-ecosystem/).
7. **Training a foundational model is prohibitively expensive for our needs.** We’ve raised $400m, and training a competitive foundational model would cost somewhere between $3m to $100m to match the general models provided by Anthropic or OpenAI

## Explore

Large Language Models operate on top of a foundational model. Training these foundational models is exceptionally expensive, and growing more expensive over time as competition for more sophisticated models accelerates. [Meta allegedly spent $20-30m training LLaMa 2](https://www.cnbc.com/2023/10/16/metas-open-source-approach-to-ai-puzzles-wall-street-techies-love-it.html), up from about $3m training costs for LLaMa 1. OpenAI’s GPT-4 [allegedly cost $100m to train](https://www.wired.com/story/openai-ceo-sam-altman-the-age-of-giant-ai-models-is-already-over/). With some nuance related to the quality of corpus and its relevance to the task at hand, [larger models outperform smaller models](https://arxiv.org/abs/2309.16583), so there’s not much incentive to train a smaller foundational model unless you have a large, unique dataset to train against, and even in that case you might be better off fine-tuning or in-context learning (ICL).

[Anthropic charges](https://www.anthropic.com/api) between $0.25 and $15 per million tokens of input, and a bit more for output tokens. [OpenAI charges](https://openai.com/api/pricing) between $0.50 and $60 per million tokens of input, and a bit more for output tokens. The average English word is about 1.3 tokens, which means you can do a significant amount of LLM work while spending less than most venture funded startups spend on snacks.

There’s [significant debate on whether LLMs have reached a point where their performance improvements will slow](https://garymarcus.substack.com/p/evidence-that-llms-are-reaching-a). Much like the ongoing debate around whether Moore’s Law has died, it’s unclear how much LLM performance will improving going forward. From a cost to train perspective, it’s unlikely that companies can continue to improve foundational models merely by spending more money on compute. Few companies can tolerate a $1B training cost, and fewer will tolerate a $10B training cost, but it’s hard to imagine a world where any companies are building $100B models. However, algorithmic improvements and investment in datasets may well drive improvements without driving up compute costs. The only high confidence prediction you can make in this space is that it’s likely model improvement will double one or two more times over the next 3 years, after which it _might_ continue doubling at that rate or it _might_ plateau at that level of performance: either outcome is plausible.

For some decisions, there’s a strategic imperative to get it right from the beginning. For example, migrating from AWS to Azure is very expensive due to the degree of customization and lock-in. However, LLMs don’t appear to be in this category. Talking with industry peers, the majority of companies are experimenting with a variety of models from Anthropic, OpenAI and elsewhere (e.g. [Mistral](https://mistral.ai/)). Behaviors do vary across models, but it’s also true that behavior of existing models varies over time (e.g. [GPT 3.5 allegedly got “lazier” over time](https://arstechnica.com/information-technology/2023/12/is-chatgpt-becoming-lazier-because-its-december-people-run-tests-to-find-out/)), which means the overhead of dealing with model differences is unavoidable even if you only adopt one.
Vendor lock-in for models is low from a technical perspective.
However, regulatory requirements--like updating Data Processing Agreements--introduce some friction when switching providers.

Although there’s an ongoing investment boom in artificial intelligence, most scaled technology companies are still looking for ways to leverage these capabilities beyond the obvious, widespread practices like adopting [Github Copilot](https://github.com/features/copilot). For example, [Stripe is investing heavily in LLMs for internal productivity](https://podcasts.apple.com/us/podcast/build-ai-products-at-on-ai-companies-with-emily/id1668002688?i=1000644619725), including presumably relying on them to perform some internal tasks that would have previously been performed by an employee such as verifying a company’s website matches details the company supplied in their onboarding application, but it’s less clear that they have yet found an approach to  meaningfully shift their product, or their product’s user experience, using LLMs.

Looking at ridesharing companies more specifically, there don’t appear to be any breakout industry-specific approaches either. Uber is similarly adopting LLMs for internal productivity, and some operational efficiency improvements as documented in their [August, 2023 post describing their internal developer and operations productivity investments using LLMs](https://www.uber.com/blog/the-transformative-power-of-generative-ai/) and [May, 2024 post describing those efforts in more detail](https://www.uber.com/blog/from-predictive-to-generative-ai/).
````

## File: llm/23000_dx-llm-model.md
````markdown
# Modeling impact of LLMs on Developer Experience.
url: https://craftingengstrategy.com/llm-adoption-model

In [How should you adopt Large Language Models?](https://craftingengstrategy.com/llm-adoption-strategy/) (LLMs), we considered how
LLMs might impact a company's developer experience. To support that exploration, I've developed a [system model](https://craftingengstrategy.com/systems-modeling/)
of the software development process at the company.

In this chapter, we'll work through:

1. Summary results from this model
2. How the model was developed, both sketching and building the model in a spreadsheet.
    (As discussed in [the overview of systems modeling](https://craftingengstrategy.com/systems-modeling/),
    I generally would recommend against using spreadsheets to develop most models,
    but it's educational to attempt doing so once or twice.)
3. Exercise the model to see what it has to teach us

Let's get into it.

---

*This is an exploratory, draft chapter for a book on engineering strategy that I’m brainstorming in*
*[#eng-strategy-book](https://lethain.com/tags/eng-strategy-book/).*
*As such, some of the links go to other draft chapters, both published drafts and very early, unpublished drafts.*

## Learnings

This model's insights can be summarized in three charts.
First, the baseline chart, which shows an eventual equilibrium between errors discovered
in production and tickets that we've closed by shipping to production.
This equilibrium is visible because tickets continue to get opened, but the total number of
closed tickets stops increasing.

![The image is a line chart titled "Started Coding, Tested Code, Deployed Code and Closed Ticket." It features five different colored lines representing various stages or statuses:

1. **Open Tickets (Blue Line)**: Starts at 10 and gradually increases to 25. This line shows a steady upward trend.

2. **Started Coding (Red Line)**: Begins at 0, rises sharply to 5, and then remains constant.

3. **Tested Code (Yellow Line)**: Not shown in the visible part of the chart, indicating possibly no data or a very low, constant value.

4. **Deployed Code (Green Line)**: This line is flat at the bottom, indicating no visible changes over time.

5. **Closed Ticket (Orange Line)**: Starts at 0, quickly rises to 5, and remains constant.

Overall, the chart displays trends in ticket statuses and coding phases over time, with open tickets increasing, while started and closed tickets remain constant.](https://craftingengstrategy.com/static/blog/strategy/dx-chart-1.png)

<p class="img-desc i tc f6">Baseline chart where closed tickets quickly stops increasing</p>

Second, we show that we can shift that equilibrium by reducing the error rate in production.
Specifically, the first chart models 25% of closed tickets in production experiencing an error,
whereas the second chart models only a 10% error rate.
The equilibrium returns, but at a higher value of shipped tickets.

![The image is a line graph titled "Started Coding, Tested Code, Deployed Code and Closed Ticket". It tracks the status of tickets over time, with lines representing different stages of coding and ticket statuses.

- **Axes**: 
  - The x-axis is not labeled but likely represents time or stages of development.
  - The y-axis represents the number of tickets, with increments marked from 0 to 20.

- **Legend**:
  - Blue line: Open Tickets
  - Red line: Started Coding
  - Yellow line: Tested Code
  - Green line: Deployed Code
  - Orange line: Closed Ticket

- **Data points**:
  - The blue line (Open Tickets) starts at just above 10 and gradually increases towards 20.
  - The orange line (Closed Ticket) starts at 0 and steadily increases to 10, then levels off.
  - The green line (Deployed Code) remains constant at a low number, close to 0.
  - There are no visible red (Started Coding) or yellow (Tested Code) lines on the chart, suggesting no data or their lines being too low to be visible.

This graph likely visualizes stages of a ticketing system in software development or a similar process.](https://craftingengstrategy.com/static/blog/strategy/dx-chart-2.png)

<p class="img-desc i tc f6">Reduced error rates delay, but don't prevent, reaching equilibrium of closed tickets</p>

Finally, we can see that even tripling the rate that we start and test tickets
doesn't meaningfully change the total number of completed tickets,
as modeled in this third chart.

![The image is a line chart titled "Started Coding, Tested Code, Deployed Code and Closed Ticket." It tracks different stages of a process over time. There are five lines, each representing a different category:

1. **Open Tickets (Blue Line):** 
   - Shows a fluctuating pattern with numbers generally between 10 and 15, peaking towards the end around 15.
   - The line zigzags, indicating variability in the number of open tickets.

2. **Started Coding (Red Line):** 
   - Displays a fluctuating pattern peaking several times, but mainly staying between 0 and 5.
   - Reflects the number of instances where coding has started.

3. **Tested Code (Yellow Line):**
   - Absent or negligible values on the chart, suggesting no significant data points for tested code.

4. **Deployed Code (Green Line):**
   - A flat line at the bottom indicating no deployment activity or stable deployment with negligible variation.

5. **Closed Ticket (Orange Line):**
   - Starts at zero and shows a steady increase, reaching a flat line at about the number 5.
   - Indicates a consistent effort to close tickets over time.

The chart uses a key on the right to identify which color corresponds to each category. The general trend suggests fluctuating open tickets, inconsistent coding activities, and steady closure of tickets.](https://craftingengstrategy.com/static/blog/strategy/dx-chart-4.png)

<p class="img-desc i tc f6">Starting or testing tickets faster creates noise but not progress</p>

The constraint on this system is errors discovered in production,
and any technique that changes something else doesn't make much of an impact.
Of course, this is just _a model_, not reality. There are many nuances
that models miss, but this helps us focus on what probably matters the most,
and in particular highlights that any approach that increases development velocity
while also increasing production error rate is likely net-negative.

With that summary out of the way, now we can get into developing the model itself.

## Sketch

Modeling in a spreadsheet is labor intensive, so we want to iterate as much as possible
in the sketching phase, before we move to the spreadsheet.
In this case, we're working with [Excalidraw](https://excalidraw.com/).

![The image is a flowchart depicting a software development process. It consists of five stages represented as rounded rectangles connected by arrows:

1. **Open Tickets** - The starting point where tickets or tasks are listed.
2. **Start Coding** - The phase where coding begins on the tasks.
3. **Tested Code** - The phase where the written code is tested.
4. **Deployed Code** - The phase where tested code is deployed.
5. **Closed Ticket** - The endpoint where tickets are closed after successful deployment.

There are additional arrows indicating feedback loops:

- From "Tested Code" back to "Start Coding," labeled as "Testing found error."
- From "Deployed Code" back to "Start Coding," labeled as "Deployment exposed error."
- From "Closed Ticket" back to "Start Coding," labeled as "Error found in production."

These loops indicate errors found at different stages, requiring a return to the coding stage.](https://craftingengstrategy.com/static/blog/strategy/llm-dx-model-1.png)

<p class="img-desc i tc f6">Five stages of development, with errors causing backwards movement</p>

I sketched five stocks to represent a developer's workflow:

1. `Open Tickets` is tickets opened for an engineer to work on
2. `Start Coding` is tickets that an engineer is working on
3. `Tested Code` is tickets that have been tested
4. `Deployed Code` is tickets than have been deployed
5. `Closed Ticket` is tickets that are closed after reaching production

There are four flows representing tickets progressing through this development process from left to right.
Additionally, there are three exception flows that move from right to left:

1. `Testing found error` represents a ticket where testing finds an error, moving the ticket backwards to `Start Coding`
2. `Deployment exposed error` represents a ticket encountering an error during deployment, where it's moved backwards to `Start Coding`
3. `Error found in production` represents a ticket encountering a production error, which causes it to move all the way back to the beginning as a new ticket

One of your first concerns seeing this model might be that it's embarrassingly simple.
To be honest, that was my reaction when I first looked at it, too.
However, it's important to recognize that feeling and then dig into whether it matters.

This model is quite simple, but in the next section we'll find that it reveals several
counter-intuitive insights into the problem that will help us avoid erroneously viewing the
tooling as a failure if time spent testing increases.
The value of a model is in refining our thinking, and simple models are usually more effective
at refining thinking across a group than complex models, simply because complex models are fairly
difficult to align a group around.

## Reason

As we start to look at this sketch, the first question to ask is how might LLM-based tooling show an improvement?
The most obvious options are:

1. Increasing the rate that tasks flow from `Starting coding` to `Tested code`.
    Presumably these tools might reduce the amount of time spent on implementation.
2. Increasing the rate that `Tested code` follows `Testing found errors` to return to `Starting code`
    because more comprehensive tests are more likely to detect errors.
    This is probably the first interesting learning from this model: if the adopted tool works well, it's likely that we'll spend
    _more_ time in the testing loop, with a long-term payoff of spending less time solving problems in production where it's more expensive.
    This means that slower testing might be a successful outcome rather than a failure as it might first appear.

    A skeptic of these tools might argue the opposite, that LLM-based tooling will cause more issues to be identified "late"
    after deployment rather than early in the testing phase. In either case, we now have a clear goal to measure to evaluate
    the effectiveness of the tool: reducing the `Error found in production` flow. We also know _not_ to focus on the
    `Testing found error` flow, which should probably increase.
3. Finally, we can also zoom out and measure the overall time from `Start Coding` to `Closed Ticket` for tasks
    that don't experience the `Error found in production` flow for at least the first 90 days after being completed.

These observations capture what I find remarkable about systems modeling: even a very simple model
can expose counter-intuitive insights. In particular, the sort of insights that build conviction to push
back on places where intuition might lead you astray.

## Model

For this model, we'll be modeling it directly in a spreadsheet, specifically Google Sheets.
The completed spreadsheet model [is available here](https://docs.google.com/spreadsheets/d/1YAego3JiNCUE15GeL_3GQfYmrE1jG9dVF6yzu-mAxLw/edit?gid=1325089804#gid=1325089804).
As discussed in [Systems modeling to refine strategy](https://craftingengstrategy.com/systems-modeling/), spreadsheet modeling
is brittle, slow and hard to iterate on. I generally recommend that folks attempt to model something in a spreadsheet
to get an intuitive sense of the math happening in their models, but I would almost always choose any tool other
than a spreadsheet for a complex model.

This example is fairly tedious to follow, and you're entirely excused if you decide to pull open the sheet itself,
look around a bit, and then skip the remainder of this section.
If you are hanging around, it's time to get started.

The spreadsheet we're creating has three important worksheets:

* *Model* represents the model itself
* *Charts* holds charts of the model
* *Config* holds configuration values separately from the model to ease exercising the model after we've built it

Going to the model worksheet, we want to start out by initializing each of the columns to the starting value.

![The image displays a simple table with two rows and five columns. 

- The first row contains headers: "Open Tickets," "Started Coding," "Tested Code," "Deployed Code," and "Closed Ticket."
- The second row provides corresponding numerical data:
  - "Open Tickets": 10
  - "Started Coding": 0
  - "Tested Code": 0
  - "Deployed Code": 0
  - "Closed Ticket": 0

The layout suggests a workflow or tracking system where open tickets are progressing through different stages of completion.](https://craftingengstrategy.com/static/blog/strategy/dx-model-screeshot-0.png)

<p class="img-desc i tc f6">Initial values of a systems model</p>

While we'll use formulae for subsequent rows, the first row should contain literal values. I often start with
a positive value in the first column and zeros in the other columns, but that isn't required.
You can start with whatever starting values are more useful for studying the model that you're building.

With the initial values set, we're now going to implement the model in two passes.
First, we'll model the left-to-right flows, which represent the standard development process.
Second, we'll model the right-to-left flows, which represent exceptions in the process.

### Modeling left-to-right

We'll start by modeling the interaction between the first two nodes: `Open Tickets` and `Started Coding`.
We want to have open tickets increased over time at a fixed rate, so let's add a value in the config worksheet
for `TicketOpenRate`, starting with `1`.

Moving to the second stock, we want to start work on open tickets as long as we have at most `MaxConcurrentCodingNum` open tickets.
If we have more than `MaxConcurrentCodingNum` tickets that we're working on, then we don't start working on any new tickets.
To do this, we actually need to create an intermediate value (represented using an italics column name) to determine how
many should be created by checking if the current in started tickets is at maximum (another value in the config sheet)
or if we should increment that by one.

That looks like:

    // Config!$B$3 is max started tickets
    // Config!$B$2 is rate to increment started tickets
    // $ before a row or column, e.g. $B$3 means that the row or column
    //   always stays the same -- not incrementing -- even when filled
    //   to other cells
    = IF(C2 >= Config!$B$3, 0, Config!$B$2)

This also means that our first column, for `Open Tickets` is decremented by the number of tickets that
we're started coding:

    // This is the definition of `Open Tickets`
    =A2 + Config!$B$1 - B2

Leaving us with these values.

![The image shows a spreadsheet with six column headers: "Open Tickets," "StartCodingMore?," "Started Coding," "Tested Code," "Deployed Code," and "Closed Ticket." The data under each column consists of numeric values:

- **Open Tickets**: Starts at 10 and increases sequentially by 1 for each row, ending at 28 (from row 2 to 20).
  
- **StartCodingMore?**: Alternates between 0 and 1 for the first few rows, then consistently holds the value 0 starting from row 6 onward.

- **Started Coding**: Increases from 0 to 3 over the first few rows.

- **Tested Code**: Starts at 0 in the second row and reaches 3 by row 5, maintaining that value for the following entries.

- **Deployed Code** and **Closed Ticket**: Both columns have 0s, with no values beyond the second row.

The spreadsheet appears to track progress in a workflow with columns indicating the status of coding tickets.](https://craftingengstrategy.com/static/blog/strategy/dx-model-screeshot-1.png)

<p class="img-desc i tc f6">Open tickets, StartCodingMore?, and Started Coding columns in spreadsheet model</p>

Now we want to determine the number of tickets being tested at each step in the model.
To do this, we create a calculation column, `NumToTest?` which is defined as:

    // Config$B$4 is the rate we can start testing tickets
    // Note that we can only start testing tickets if there are tickets
    // in `Started Coding` that we're able to start testing
    =MIN(Config!$B$4, C3)

We then add that value to the previous number of tickets being tested.

    // E2 is prior size of the Tested Code stock
    // D3 is the value of `NumToTest?`
    // F2 is the number of tested tickets to deploy
    =E2 + D3 - F2

![The image shows a spreadsheet with seven columns and twenty rows. The columns are labeled as follows:

1. **Open Tickets**
2. **Started Coding**
3. **NumToTest?**
4. **Tested Code**
5. **Deployed Code**
6. **Closed Ticket**

The data begins from the second row:

- **Open Tickets** starts at 10 and quickly increases to 11 where it remains constant.
- **Started Coding** begins at 0 and then transitions to 1 where it stays constant.
- **NumToTest?** follows the same pattern as Started Coding, starting at 0 then switching to 1.
- **Tested Code** starts at 0 and increments by 1 with each row, reaching 18 in the last row.
- **Deployed Code** and **Closed Ticket** remain at 0 throughout the data.

The cells under "Open Tickets" and "NumToTest?" are shaded in grey.](https://craftingengstrategy.com/static/blog/strategy/dx-model-screeshot-2.png)

<p class="img-desc i tc f6">Started Coding, NumToTest?, and Tested Code columns in spreadsheet model</p>

Spreadsheet showing three columns of systems modeling

Moving on to deploying code, let's keep things simple and start out by assuming that every tested change
is going to get deployed. That means the calculation for `NumToDeploy?` is quite simple:

    // E3 is the number of tested changes
    =E3

Then the value for the `Deployed Code` stock is simple as well:

    // G2 is the prior size of Deployed Code
    // F3 is NumToDeploy?
    // H2 is the number of deployed changes in prior round
    =G2+F3-H2

![The image shows a spreadsheet with seven columns and several rows of data. Here’s a detailed breakdown:

**Columns:**
1. **Open Tickets**: Starts with 10, then lists 11 for the remaining rows.
2. **Started Coding**: The first entry is 0, followed by all 1s.
3. **Tested Code**: The first entry is 0, followed by all 1s.
4. **NumToDeploy?**: Displays increasing numbers starting from 0 up to 18.
5. **Deployed Code**: The first entry is 0, followed by all 1s.
6. **NumToClose?**: Displays increasing numbers starting from 0 up to 18.
7. **Closed Ticket**: All entries are 0.

The data appears to be related to a software development or IT project management process, tracking ticket statuses through various stages like coding, testing, and deployment. The numbers suggest a sequential progression in the "NumToDeploy?" and "NumToClose?" columns.](https://craftingengstrategy.com/static/blog/strategy/dx-model-screeshot-3.png)

<p class="img-desc i tc f6">NumToDeploy? and Deployed Code columns in spreadsheet model</p>

Now we're on to the final stock.
We add the `NumToClose?` calculation, which assumes that all deployed changes are now closed.

    // G3 is the number of deployed changes
    =G3

This makes the calculation for the `Closed Tickets` stock:

    // I2 is the prior value of Closed Tickets
    // H3 is the NumToClose?
    =I2 + H3

With that, we've now modeled the entire left-to-right flows.

![The image displays a spreadsheet with six columns and twenty rows of data starting from row 2. 

**Columns:**
1. **Open Tickets:** Lists the number 11 throughout, except for the first row where it is 10.
2. **Started Coding:** Displays a mix of zeros and ones. The first row contains a 0, and all subsequent rows have a 1.
3. **Tested Code:** Contains mostly ones, starting with a 0 in the first row.
4. **Deployed Code:** Similar to the Tested Code column, with a 0 in the first row and ones in all other rows.
5. **NumToClose?:** Reflects the pattern from the previous columns, starting with a 0 and ones in the rest of the rows.
6. **Closed Ticket:** Displays sequential numbers starting from 0 in the first row up through 18 in the last row.

**Rows:**
- Row 2 to 20 show a generally consistent flow of ones from the second to fifth columns, with the Open Tickets consistently showing 11, except in the initial row.

The layout suggests a workflow or process tracking system where the progression of ticket status is recorded across various stages.](https://craftingengstrategy.com/static/blog/strategy/dx-model-screeshot-4.png)

<p class="img-desc i tc f6">Entirety of left-to-right flows in spreadsheet model</p>

The left-to-right flows are simple, with a few constrained flows and a very scalable flows, but overall we see things
progressing through the pipeline evenly.
All that is about to change!

### Modeling right-to-left

We've now finished modeling the happy path from left to right.
Next we need to model all the exception paths where things flow right to left.
For example, an issue found in production would cause a flow from `Closed Ticket`
back to `Open Ticket`.
This tends to be where models get interesting.

There are three right-to-left flows that we need to model:

1. `Closed Ticket` to `Open Ticket` represents a bug discovered in production.
2. `Deployed Code` to `Start Coding` represents a bug discovered during deployment.
3 `Tested Code` to `Start Coding` represents a bug discovered in testing.

To start, we're going to add configurations defining the rates of those flows.
These are going to be percentage flows, with a certain percentage of the target stock
triggering the error condition rather than proceeding. For example, perhaps 25% of the
`Closed Tickets` are discovered to have a bug each round.

![The image shows a spreadsheet with two visible columns, A and B, and seven rows filled with data. It contains the following information:

- **Column A (Labels):**
  - Row 1: TicketOpenRate
  - Row 2: StartCodingRate
  - Row 3: MaxConcurrentCodingNum
  - Row 4: TicketTestRate
  - Row 5: ErrorsInProd
  - Row 6: ErrorsInDeploy
  - Row 7: ErrorsInTest

- **Column B (Values):**
  - Rows 1, 2, and 4 have the value "1".
  - Row 3 has the value "3".
  - Rows 5, 6, and 7 each have the value "0.25".

Columns C through E are empty, and the cells appear to have a gray shading, except for rows 5 through 7, which have white shading.](https://craftingengstrategy.com/static/blog/strategy/dx-model-screeshot-5.png)

<p class="img-desc i tc f6">Introducing three additional values in model configuration</p>

These are fine starter values, and we'll experiment with how adjusting them changes the model in the *Exercise* section below.

Now we'll start by modeling errors discovered in production, by adding a column
to model the flow from `Closed Tickets` to `Open Tickets`, the `ErrorsFoundInProd?` column.

    // I3 is the number of Closed Tickets
    // Config!$B$5 is the rate of errors
    =FLOOR(I3 * Config!$B$5)

Note the usage of `FLOOR` to avoid moving partial tickets.
Feel free to skip that entirely if you're comfortable with the concept of fractional tickets, fractional deploys, and so on.
This is an aesthetic consideration, and generally only impacts your model if you choose overly small starting values.

This means that our calculation for `Closed Ticket` needs to be
updated as well to reduce by the prior row's result for `ErrorsFoundInProd?`:

    // I2 is the prior value of ClosedTicket
    // H3 is the current value of NumToClose?
    // J2 is the prior value of ErrorsFoundInProd?
    =I2 + H3 - J2

We're not quite done, because we _also_ need to add the prior row's value of `ErrorsInProd?`
into `Open Tickets`, which represents the errors' flow from closed to open tickets.
Based on this change, the calculation for `Open Tickets` becomes:

    // A2 is the prior value of Open Tickets
    // Config!$B$1 is the base rate of ticket opening
    // B2 is prior row's StartCodingMore?
    // J2 is prior row's ErrorsFoundInProd?
    =A2 + Config!$B$1 - B2 + J2

Now we have the full errors in production flow represented in our model.

![The image is a screenshot of a spreadsheet with the following columns and data:

1. **Column A (Open Tickets):** Numbers 10 to 25 in sequence over 20 rows.

2. **Column B (StartCodingMore?):** 
   - Row 2 has 0, the rest have 1.

3. **Column C (Started Coding):**
   - Row 2 has 0, the rest have 1.

4. **Column E (Tested Code):**
   - Row 2 has 0, the rest have 1.

5. **Column G (Deployed Code):**
   - Row 2 has 0, the rest have 1.

6. **Column I (Closed Ticket):**
   - Row 2 has 0, row 3 has 1, row 4 has 2, row 5 has 3, row 6 and onwards have 4.

7. **Column J (ErrorsFoundInProd?):**
   - Row 2 and 3 have 0, the rest have 1.

The data seems to track the progress of tickets through stages like starting, coding, testing, deploying, and closing, with an indication of whether errors were found in production.](https://craftingengstrategy.com/static/blog/strategy/dx-model-screeshot-6.png)

<p class="img-desc i tc f6">Modeling ErrorsFoundInProd? in spreadsheet model</p>

Next, it's time to add the `Deployed Code` to `Start Coding` flow.
Start by adding the `ErrorsFoundInProd?` calculation:

    // G3 is deployed code
    // Config!$B$6 is deployed error rate
    =FLOOR(G3 * Config!$B$6)

Then we need to update the calculation for `Deployed Code` to decrease by the
calculated value in `ErrorsFoundInProd?`:

    // G2 is the prior value of Deployed Code
    // F3 is NumToDeploy?
    // H2 is prior row's NumToClose?
    // I2 is ErrorsFoundInDeploy?
    =G2 + F3 - H2 - I2

Finally, we need to increase the size of `Started Coding` by the same value,
representing the flow of errors discovered in deployment:

    // C2 is the prior value of Started Coding
    // B3 is StartCodingMore?
    // D2 is prior value of NumToTest?
    // I2 is prior value of ErrorsFoundInDeploy?
    =C2 + B3 - D2 + I2

We now have the working flow representing errors in production.

![The image is a screenshot of a spreadsheet with data organized in columns and rows. Here’s a detailed description:

### Columns:
- **A (Open Tickets):** Lists numbers, starting from 10 and incrementing by 1 down to 25.
- **C (Started Coding):** Contains binary data, mostly 1s, except for the first row which is 0.
- **E (Tested Code):** Similar to the "Started Coding" column, it contains 1s except for the first row which is 0.
- **G (Deployed Code):** Also mirrors the previous two columns with 1s and the first entry as 0.
- **H (NumToClose?):** Consistently 0s and 1s as per previous patterns.
- **I (ErrorsFoundInDeploy?):** Contains 0s, indicating no errors were found.
- **J (Closed Ticket):** Starts with 0 and increments to 4 by the fourth row, staying 4 thereafter.

### Characteristics:
- Each column apart from "Open Tickets" primarily shows a binary pattern of data.
- The sequence at the start of columns B, D, F, and J shows a single zero evolving into ones or higher numbers, indicating progression or status updates in a process flow.

This spreadsheet appears to track a workflow or a ticketing system with stages like coding, testing, deployment, and closure, with a focus on whether errors were encountered.](https://craftingengstrategy.com/static/blog/strategy/dx-model-screeshot-7.png)

<p class="img-desc i tc f6">DeployedCode, NumToClose?, and ErrorsFoundInDeploy? columns in spreadsheet model</p>

Finally, we can added the `Tested Code` to `Started Coding` flow.
This is pretty much the same as the prior flow we added,
starting with adding a `ErrorsFoundInTest?` calculation:

    // E3 is tested code
    // Config!$B$7 is the testing error rate
    =FLOOR(E3 * Config!$B$7)

Then we update `Tested Code` to reduce by this value:

    // E2 is prior value of Tested Code
    // D3 is NumToTest?
    // G2 is prior value of NumToDeploy?
    // F2 is prior value of ErrorsFoundInTest?
    =E2 + D3 - G2 - F2

And update `Started Coding` to increase by this value:

    // C2 is prior value of Started Coding
    // B3 is StartCodingMore?
    // D2 is prior value of NumToTest?
    // J2 is prior value of ErrorsFoundInDeploy?
    // F2 is prior value of ErrorsFoundInTest?
    = C2 + B3 - D2 + J2 + F2

Now this last flow is instrumented.

![The image shows a spreadsheet with data organized into columns and rows. Here's a detailed breakdown:

### Column Headers:
- **A:** Open Tickets
- **B:** StartCodingMore?
- **C:** Started Coding
- **D:** NumToTest?
- **E:** Tested Code
- **F:** ErrorsFoundInTest?
- **H:** Deployed Code
- **K:** Closed Ticket

### Rows:
- Row 1 contains the headers.
- Rows 2 to 20 provide numerical data under each header.

### Data Details:
- **Open Tickets (Column A):** Ranges from 10 to 25, increasing by 1 per row.
- **StartCodingMore? (Column B):** Mostly 1s, with a 0 in row 2.
- **Started Coding (Column C):** All entries are 1s.
- **NumToTest? (Column D):** Mostly 1s, with a 0 in row 2.
- **Tested Code (Column E):** All entries are 1s.
- **ErrorsFoundInTest? (Column F):** All entries are 0s.
- **Deployed Code (Column H):** Most entries are 1s, with a 0 in row 2.
- **Closed Ticket (Column K):** Starts at 0 in row 2 and increases gradually, reaching 4 in row 5 and remaining constant.

### Additional Notes](https://craftingengstrategy.com/static/blog/strategy/dx-model-screeshot-8.png)

<p class="img-desc i tc f6">Modeling ErrorsFoundInTest? in spreadsheet model</p>

With that, we now have a complete model that we can start exercising!
This exercise demonstrated both that it's _quite possible_ to represent
a meaningful model in a spreadsheet, but also the challenges of doing so.

While developing this model, a number of errors became evident. Some of them
I was able to fix relatively easily, and even more I left unfixed because fixing
them makes the model _even harder_ to reason about. This is a good example of why
I encourage developing one or two models in a spreadsheet, but I ultimately don't
believe it's the right mechanism to work in for most people:
even very smart people make errors in their spreadsheets, and catching those errors
is exceptionally challenging.

## Exercise

Now that we're done building this model, we can finally start the fun part: exercising it.
We'll start by creating a simple bar chart showing the size of each stock at each step.
We are going to expressly _not_ show the intermediate calculation columns such as `NumToTest?`,
because those are implementation details rather than particularly interesting.

Before we start tweaking the values , let's look at the baseline chart.

![The image is a line graph titled "Started Coding, Tested Code, Deployed Code and Closed Ticket." It compares different software development stages and tickets over a period (possibly days or weeks).

The legend identifies the lines:
- **Open Tickets (blue line)**: Starts around 11, remains steady, then rises sharply to 25, indicating an increase in the number of open tickets over time.
- **Started Coding (red line)**: Begins at 0, increases to 5, then levels out, showing coding activity that starts and quickly stabilizes.
- **Tested Code (yellow line)**: Not visible, indicating no or minimal data for this category.
- **Deployed Code (green line)**: Starts at 0 and remains flat, indicating no deployment activity recorded.
- **Closed Ticket (orange line)**: Increases to 5 and then stabilizes, showing closed tickets matching the started coding activity.

Overall, the graph shows a high rise in open tickets, with some initial activity in coding and closing tickets, while testing and deployment remain static.](https://craftingengstrategy.com/static/blog/strategy/dx-chart-1.png)

<p class="img-desc i tc f6">Baseline chart where closed tickets quickly stops increasing</p>

The most interesting thing to notice is that our current model doesn't actually increase the number of closed
tickets over time. We actually just get further and further behind over time, which isn't too exciting.

So let's start modeling the first way that LLMs might help, reducing the error rate in production.
Let's shift `ErrorsInProd` from `0.25` down to `0.1`, and see how that impacts the chart.

![The image is a line graph titled “Started Coding, Tested Code, Deployed Code and Closed Ticket.” It displays data related to different stages in a software development process. The x-axis represents the timeline, while the y-axis represents the number of actions or tickets.

There are five lines in different colors, each representing a different category:

1. **Open Tickets (Blue Line)**: Starts at 10 and remains constant initially, then increases linearly towards 20.
2. **Started Coding (Red Line)**: Starts at 0, rises sharply to 10, then flattens.
3. **Tested Code (Yellow Line)**: Remains consistently at 0 throughout the timeline.
4. **Deployed Code (Green Line)**: Starts at 0 and quickly rises to a value slightly above 0, then stays flat.
5. **Closed Ticket (Orange Line)**: Starts at 0, rises linearly to approximately 11, and stays constant.

The graph indicates different progress stages with only "Open Tickets" showing a continued upward trend.](https://craftingengstrategy.com/static/blog/strategy/dx-chart-2.png)

<p class="img-desc i tc f6">Reduced error rates delays, but doesn't prevent, reaching equilibrium of closed tickets</p>

We can see that this allows us to make more progress on closing tickets, although
at some point equilibrium is established between closed tickets and the error rate in production,
preventing further progress. This does validate that reducing error rate in production matters.
It also suggests that as long as error rate is a function of everything we've previously shipped,
we are eventually in trouble.

Next let's experiment with the idea that LLMs allow us to test more quickly,
tripling `TicketTestRate` from `1` to `3`. It turns out, increasing testing rate doesn't change anything at all,
because the current constraint is in starting tickets.

![The image is a line chart titled "Started Coding, Tested Code, Deployed Code and Closed Ticket." It features five different lines representing various ticket statuses:

1. **Open Tickets (blue line):** Starts at 10, remains steady, and then rises to about 18.
2. **Started Coding (red line):** Static at 10 throughout.
3. **Tested Code (yellow line):** A flat line at 0.
4. **Deployed Code (green line):** Also remains constant at 2.
5. **Closed Ticket (orange line):** Starts from 0 and rises sharply to 10, remains steady.

The chart visually compares the progression or status of different stages of coding and ticket handling over a certain period.](https://craftingengstrategy.com/static/blog/strategy/dx-chart-3.png)

<p class="img-desc i tc f6">Changing testing rate doesn't model's behavior</p>

So, let's test that. Maybe LLMs make us faster in starting tickets because _overall_ speed of development goes down.
Let's model that by increasing `StartCodingRate` from `1` to `3` as well.

![The image is a line chart titled "Started Coding, Tested Code, Deployed Code and Closed Ticket." It consists of five lines representing different stages of a project or workflow, as indicated by the legend on the right:

1. **Open Tickets (Blue Line):** This line fluctuates between 9 and 17, showing a consistent up-and-down pattern throughout the timeline.

2. **Started Coding (Red Line):** This line starts at 0, peaks at 5, and follows a sawtooth pattern with multiple up-and-down movements, hovering mostly between 0 and 5.

3. **Tested Code (Yellow Line):** A flat line at 0, indicating that there are no tickets at this stage in the timeline.

4. **Deployed Code (Green Line):** Another flat line at 0, similar to the Tested Code, indicating no activity at this stage.

5. **Closed Ticket (Orange Line):** This line rises steadily, starting from 0 and reaching 5, indicating a linear increase in closed tickets over time.

The chart seems to represent the progress of tickets through different stages of a process, with open tickets being most volatile and closed tickets showing a steady increase.](https://craftingengstrategy.com/static/blog/strategy/dx-chart-4.png)

<p class="img-desc i tc f6">Starting or testing tickets faster creates noise but not progress</p>

This is a fascinating result, because tripling development and testing velocity has changed how much work we start,
but ultimately the real constraint in our system is the error discovery rate in production.

By exercising this model, we find an interesting result. To the extent that our error rate is a function of the volume
of things we've shipped in production, shipping faster doesn't increase our velocity at all.
The only meaningful way to increase productivity in this model is to reduce the error rate in production.

Models are imperfect representations of reality, but this one gives us a clear sense of what matters the most:
if we want to increase our velocity, we have to reduce the rate that we discover errors in production.
That might be reducing the error rate as implied in this model, or it might be ideas that exist outside of this model.
For example, the model doesn't represent this well, but perhaps we'd be better off iterating more on fewer things to avoid this scenario.
If we make multiple changes to one area, it still just represents one implemented feature, not many implemented features, and the overall error
rate wouldn't increase.
````

## File: llm/24000_wardley-llm-ecosystem.md
````markdown
# Wardley mapping the LLM ecosystem.
url: https://craftingengstrategy.com/wardley-llm-ecosystem

In [How should you adopt LLMs?](https://craftingengstrategy.com/llm-adoption-strategy/), we explore how a theoretical ride sharing company,
Theoretical Ride Sharing, should adopt Large Language Models (LLMs).
Part of that strategy's diagnosis depends on understanding the expected evolution of 
the LLM ecosystem, which we've built a [Wardley map](https://craftingengstrategy.com/wardley-mapping/) to better explore.

This map of the LLM space focuses on how product companies should address the
proliferation of model providers such as Anthropic, Google and OpenAI,
as well as the proliferation of LLM product patterns like agentic workflows, Retrieval Augmented Generation (RAG),
and running [evals to maintain performance as models change](https://github.com/openai/evals).

---

*This is an exploratory, draft chapter for a book on engineering strategy that I'm brainstorming in [#eng-strategy-book](https://lethain.com/tags/eng-strategy-book/).*
*As such, some of the links go to other draft chapters, both published drafts and very early, unpublished drafts.*

## Reading this document

To quickly understand the analysis within this Wardley Map,
read from top to bottom to understand this analysis.
If you want to understand how this map was _written_, then you should
read section by section from the bottom up, starting with Users, then Value Chains, and so on.

More detail on this structure in [Refining strategy with Wardley Mapping](https://craftingengstrategy.com/wardley-mapping/).

## How things work today

If Retrieval Augmented Generation (RAG) was the trending LLM pattern of 2023,
and you could reasonably argue that agents--or agentic workflows--are the pattern of 2024,
then it's hard to guess what the patterns of tomorrow will be, but it's likely
that there are more, new patterns coming our way.
LLMs are a proven platform today, and now are being applied widely to discover new patterns.
It's a safe bet that validating these patterns will continue to drive product companies to support additional
infrastructure components (e.g. search indexes to support RAG).

![The image is a Wardley Map, which visually represents the components and their evolution within a value chain. 

### Axes:
- **Vertical Axis (Value Chain):** Ranges from Invisible to Visible.
- **Horizontal Axis (Evolution):** Ranges from Genesis to Commodity (+utility).

### Components and Their Positioning:
1. **Product Engineer:** Positioned more toward the visible and in the custom stage.
2. **Machine Learning Infrastructure:** Similar position to Product Engineer.
3. **Security & Compliance:** Close to the visible side in the custom stage.
4. **Run evals to maintain product quality:** Between visible and invisible, in custom.
5. **Access to latest models:** More visible than hidden, in the product stage.
6. **Support for agents:** Near visible, straddling custom and product.
7. **Visibility into what is sent to models:** Positioned as visible, in the product stage.
8. **LLM vendor contract:** Very visible and in the commodity stage.
9. **Eval repository, Eval runner:** Positioned in the invisible-custom range.
10. **Indexing Pipeline:** Near the custom-product transition.
11. **Provide search index to support RAG:** Situated in custom, close to visible.
12. **Agent workflow orchestrator:** In the product stage, less visible.
13. **API Proxy:** Invisible, in the product stage.
14. **Search Index:** Between custom and product, tending toward product.

### Connections:
- Lines](https://craftingengstrategy.com/static/blog/strategy/llm-wardley-1.png)

<p class="img-desc i tc f6">Current state of LLM ecosystem</p>

This proliferation of patterns has created a significant cost for these product companies,
a problem which market forces are likely to address as offerings evolve.

## Transition to future state

Looking at the evolution of the LLM ecosystem, there are two questions
that I believe will define the evolution of the space:

1. Will LLM framework platforms for agents, RAG, and so on, remain bundled with
    model providers such as OpenAI and Anthropic?
    Or will they, instead, split with models and platforms being offered separately?
2. Which elements of LLM frameworks will be productizable in the short-term?
    For example, running evals seems like a straightforward opportunity for bundling,
    as would providing _some_ degree of agent support.
    Conversely, bundling RAG might seem straightforward but most production use cases would
    require real-time updates, incurring the full complexity of operating scaled search clusters.

Depending on the answers to those questions, you might draw a very different map.
This map answers the first question by imagining that LLM platforms will decouple from model providers, while
also allowing you to license with that platform for model access rather than needing
to individually negotiate with each model provider.
It answers the second question by imagining that most non-RAG functionality will move into a bundled
platform provider. Given the richness of investment in the current space, it
seems safe to believe that every plausible combination will exist to some degree
until the ecosystem eventually stabilizes in one dominant configuration.

![The image is a Wardley map that outlines the value chain of a technology platform centered around machine learning and artificial intelligence infrastructure.

1. **Axes**:
   - The vertical axis represents the "Value Chain," ranging from "Invisible" to "Visible."
   - The horizontal axis represents the stages of evolution: "Genesis," "Custom," and "Product (+rental)."

2. **Components**:
   - **Product Engineer**: Located in the "Visible" section, it is well-defined and connected to various components.
   - **Machine Learning Infrastructure**: Also in the "Visible" region, it connects to several components.
   - **Security & Compliance** and **Access to Latest Models**: Positioned in the "Product (+rental)" section, indicating maturity and integration with vendor contracts.
   - **Run evals to maintain product quality**, **Provide search index to support RAG**, **Support for agents**, and **Visibility into what is sent to models**: These are in the visible area of the map and connected to multiple components.
   - **Indexing Pipeline** and **Search Index**: In the "Custom" phase, linked to the search index component.
   - **Agent Workflow Orchestrator**, **Eval Runner**, **Eval Repository**, and **API Proxy**: These are intermediary steps between custom developments and product offerings, contributing to platform bundling.
   - **LLM Vendor Contract**: Positioned in the "Product (+rental)" phase](https://craftingengstrategy.com/static/blog/strategy/llm-wardley-2.png)

<p class="img-desc i tc f6">Pipeline of LLM platform bundling</p>

The key drivers of this configuration are that the LLM ecosystem is investing
new patterns every year, and companies are spinning up haphazard internal solutions
to validate those patterns, but ultimately few product companies are able to effectively fund these
sorts of internal solutions in the long run.

If this map is correct, then it means eventual headwinds faced by both model providers (who are inherently
limited to providing their own subset of models) as well as narrow LLM platform providers (who
can only service a subset of LLM patterns). The likely best bet for a product company in this future
is adopting the broadest LLM pattern platforms today, and to explicitly decouple pattern platform from model provider.

## User & Value Chains

The LLM landscape is evolving rapidly, with some techniques getting introduced and reaching wide-spread adoption
within a single calendar year.
Sometimes those widely adopted techniques are _actually_ being adopted, and other times it's closer to "conference-talk driven development"
where folks with broad platforms inflate the maturity of industry adoption.

The three primary users attempting to navigate that dynamism are:

1. **Product Engineers** are looking for faster, easier solutions to deploying LLMs across
    the many, evolving parameters: new models, support for agents, solutions to offload the search
    dimensions of retrieval-augmented-generation (RAG), and so on.
1. **Machine Learning Infrastructure** team is responsible for the effective usage of the mechanisms,
    and steering product developers towards effective adoption of these tools.
    They are also, in tandem with other infrastructure engineering teams, responsible for supporting
    common elements for LLM solutions, such as search indexes to power RAG implementations.
1. **Security and Compliance** -- how to ensure models are hosted safely and securely,
    and that we're only sending approved information?
    how do we stay in alignment with rapidly evolving AI risks and requirements?

To keep the map focused on evolution rather than organizational dynamics,
I've consolidated a number of teams in slightly artificial ways,
and omitted a few teams that are certainly worth considering.
Finance needs to understand the cost and usage
of LLM usage. Security and Compliance are really different teams, with both overlapping and distinct requirements between them.
Machine Learning Infrastructure could be split into two distinct teams with somewhat conflicting perspectives
on who should own things like search infrastructure.

Depending on what _you_ want to learn from the map, you might prefer to combine, split and introduce
a different set of combinations than I've selected here.
````

## File: llm/25000_driver-onboarding-model.md
````markdown
# Modeling driving onboarding.
url: https://craftingengstrategy.com/llm-onboarding-model

The [How should you adopt LLMs?](https://craftingengstrategy.com/llm-adoption-strategy/) strategy explores how Theoretical Ride Sharing
might adopt LLMs. It builds on several models, the first is about [LLMs impact on Developer Experience](https://craftingengstrategy.com/llm-adoption-model/).
The second model, documented here, looks at whether LLMs might improve a core product and business problem: maximizing
active drivers on their ridesharing platform.

In this chapter, we'll cover:

1. Where the model of ridesharing drivers identifies opportunities for LLMs
2. How the model was sketched and developed using [lethain/systems](https://github.com/lethain/systems) package on Github
3. Exercising this model to learn from it

Let's get started.

## Learnings

An obvious assumption is making driver onboarding faster would increase the long-term number
of drivers in a market. However, this model shows that even doubling the rate that we qualify applicant drivers
as eligible has little impact on active drivers over time.

![The image is a line graph titled "ActiveDrivers Over Time." It shows the number of active drivers over a period, with the time on the x-axis and the number of active drivers on the y-axis.

- The x-axis is labeled "Time" and ranges from 0 to 250.
- The y-axis is labeled "# ActiveDrivers" and ranges from 0 to 1400.

There are two lines on the graph, each representing different scenarios:

1. **Blue Line (Base)**: 
   - Starts at the origin and gradually rises.
   - Peaks around 1400 drivers at approximately time 100.
   - Declines sharply before leveling off after time 150, stabilizing around 800 drivers.

2. **Orange Line (FastOnboarding)**:
   - Similar initial rise, but slightly steeper than the blue line.
   - Peaks at the same point as the blue line.
   - Follows a similar decline, also stabilizing around 800 drivers.

The legend is located in the top right corner, specifying "Base" for the blue line and "FastOnboarding" for the orange line. The lines overlap closely, indicating similar trends in both scenarios, with the orange line showing a slightly faster increase initially.](https://craftingengstrategy.com/static/blog/strategy/llm-ride-results-2.png)

<p class="img-desc i tc f6">Speeding up onboarding doesn't impact active drivers in the long-term</p>

Conversely, it's clear that efforts to reengage departed drivers has a significant impact
on active drivers. We believe that there are potential LLM applications that could encourage
departed drivers to return to active driving, for example mapping their rationale for departing
against our recent product changes and driver retention promotions could generate high quality,
personalized emails.

![The image is a line graph titled "ActiveDrivers Over Time." It compares two data series: "Base" and "LLM_Reengage."

1. **Axes:**
   - The x-axis represents "Time," with values ranging approximately from 0 to 250.
   - The y-axis represents the number of active drivers, labeled as "# ActiveDrivers," with values ranging approximately from 0 to 1600.

2. **Lines:**
   - **Blue Line (Base):** Starts low, increases steadily until around the 100 mark on the x-axis, where it starts to peak. After peaking, it declines gradually, leveling off past the 150 mark.
   - **Orange Line (LLM_Reengage):** Starts near the base but rises more steeply, surpassing the blue line and peaking around the same x-axis mark. It then declines, eventually leveling off higher than the blue line.

3. **Legend:**
   - The legend in the upper right corner explains the colors, with "Base" in blue and "LLM_Reengage" in orange.

The graph suggests that the "LLM_Reengage" strategy results in a higher peak and sustained number of active drivers compared to the "Base" strategy.](https://craftingengstrategy.com/static/blog/strategy/llm-ride-results-4.png)

<p class="img-desc i tc f6">Improving driver reengagement does increase active drivers</p>

Finally, the model shows that increasing either reactivation of departed or suspended drivers is significantly
less impactful than increasing both. If either rate is low, we lose an increasingly large number of drivers over time.

![The image is a line graph titled "ActiveDrivers Over Time." It plots the number of active drivers against time, ranging from 0 to 250 on the x-axis. The y-axis represents the number of active drivers, scaling from 0 to 2500.

There are three lines on the graph:

1. **Blue Line (Base):** This line starts at the origin and rises gradually, peaking at around 1000 active drivers just past the 100 mark on the time axis. It then slightly declines and stabilizes.

2. **Orange Line (LLM_Reengage):** This line starts similarly to the blue line but rises more steeply, peaking at about 1500 active drivers. It then declines and stabilizes higher than the blue line.

3. **Green Line (LLM_Unsuspend):** This line starts similar to the other lines but rises much more steeply, peaking around 2500 active drivers. It also declines and stabilizes well above the other two lines.

The legend identifies each line with its respective color and label. The graph illustrates how different strategies result in varying numbers of active drivers over time, with the green line indicating the most active drivers throughout the duration.](https://craftingengstrategy.com/static/blog/strategy/llm-ride-results-5.png)

<p class="img-desc i tc f6">Increasing reactivation rate of suspend drivers has highest impact</p>

The only meaningful opportunities for us to increase active drivers with LLMs are improving those two reactivation rates.

## Sketch

The first step in modeling a system is sketching it (using [Excalidraw](https://excalidraw.com/) here).
Here we're developing a model for onboarding and retaining drivers for a ridesharing application in one city.

![The image is a flowchart illustrating the process of transitioning drivers through various stages. 

1. **City Population**: Represents the initial pool of potential drivers.

2. **Applied Drivers**: Individuals from the city population who have applied to become drivers. An arrow leads from "City Population" to "Applied Drivers."

3. **Eligible Drivers**: Applicants who meet the necessary criteria. An arrow points from "Applied Drivers" to "Eligible Drivers." There's also a feedback loop labeled "Request missing information" going back to "Applied Drivers."

4. **Onboarded Drivers**: Eligible drivers who have completed onboarding. An arrow leads from "Eligible Drivers" to "Onboarded Drivers."

5. **Active Drivers**: Drivers who are actively working. An arrow points from "Onboarded Drivers" to "Active Drivers."

6. **Suspended Drivers**: Active drivers who have been suspended. An arrow leads from "Active Drivers" to "Suspended Drivers" with another returning arrow labeled "Remove suspension."

7. **Departed Drivers**: Drivers who have left the system. An arrow leads from "Active Drivers" to "Departed Drivers." There is also an arrow labeled "Re-engage" pointing from "Departed Drivers" back to "Active Drivers."

The flowchart visually represents the progression and potential transitions of individuals within the driver system.](https://craftingengstrategy.com/static/blog/strategy/llm-ride-model-1.png)

<p class="img-desc i tc f6">Sketch of onboarding drivers onto a ride-sharing application</p>

The stocks are:

1. `City Population` is the total population of a city
2. `Applied Drivers` are the number of people who've applied to be drivers
3. `Eligible Drivers` are the number of applied drivers who meet eligibility criteria (e.g. provided a current drivers license, etc)
4. `Onboarded Drivers` are eligible drivers who have successfully gone through an onboarding program
5. `Active Drivers` are onboarded drivers who are actually performing trips on a weekly basis
6. `Departed Drivers` were active drivers, but voluntarily stopped performing trips (e.g. took a different job)
7. `Suspended Drivers` were active drivers, but involuntarily stopped performing trips (e.g. are no longer allowed to drive on platform)

Looking at the left-to-right flows, there is a flow from each of those stocks to the following stock in the pipeline.
These are all simple one-to-one flows, with the exception of those coming from
`Active Drivers` leads to two distinct stocks: `Departed Drivers` and `Suspended Drivers`.
These represent voluntary and involuntary departures.

There are a handful of right-to-left, exception path flows to consider as well:

1. `Request missing information` represents a driver who can't be moved from `Applied Drivers` to `Eligible Drivers`
    because their provided information proved insufficient in a review process
2. `Re-engage` tracks `Departed Drivers` who have decided to start driving again, perhaps
    because of a bonus program for drivers who start driving again
3. `Remove suspension` refers to drivers who were involuntarily removed, but who are now
    allowed to return to driving

This is a fairly basic model, but let's see what we can learn from it.

## Reason

Now that we've sketched the system, we can start thinking about which flows are going to have the largest impact,
and where an LLM might increase those flows. Some observations from reasoning about it:

1. If a city's population is infinite, then what really matters in this model
    is how many new drivers we can encourage to join the system.
    On the other hand, if a city's population is finite,
    then onboarding new drivers will be essential in the early stages of coming
    online in any particular city, but long-term reengaging departed drivers
    is probably at least as important.
2. LLMs tooling could speed up validating eligible drivers. If we speed that process up enough,
    we could greatly reduce the rate of the `Request missing information` flow by identifying
    missing information in real-time rather than requiring a human to review the information later.
3. We could potentially develop LLM tooling to craft personalized messaging to `Departed Drivers`,
    that explains which of our changes since their departure might be most relevant to their reasons
    for stopping. This could increase the rate of the `Re-engage` flow
4. While we likely wouldn't want an LLM approving the removal of suspensions, we could have it look
    at requests to be revalidated, and identify promising requests to focus human attention on
    the highest potential for approval.
5. We could build LLM-powered tooling that helps a city resident decide whether they should apply
    to become a driver by answering questions they might have.

As we exercise the model later, we know that our assumptions about whether this city has already exhausted
potential drivers will quickly steer us towards a specific subset of these potential options.
If all potential drivers are already tapped, only work to reactivate prior drivers that will matter.
If there are more potential drivers, then likely activating them will be a better focus.

## Model

For this model, we'll be modeling it using the [lethain/systems](https://github.com/lethain/systems) library that I wrote.
For a more detailed introduction, I recommend working through [the tutorial in the repository](https://github.com/lethain/systems/blob/master/README.md),
but I'll introduce the basics here as well.
While `systems` is far from a perfect tool, as you experiment with different modeling techniques
like [spreadsheet-based modeling](https://craftingengstrategy.com/llm-adoption-model/) and [SageModeler](https://sagemodeler.concord.org/),
I think this approach's emphasis on rapid development and reproducible, sharable models is somewhat unique.

If you want to see the finished model,
you can find the model and visualizations in [the Jupyterhub notebook in lethain:eng-strategy-models](https://github.com/lethain/eng-strategy-models/blob/main/DriverOnboarding.ipynb).
Here we'll work through the steps behind implementing that model.

We'll start by creating a stock for the city's population,
with an initial size of 10,000.

```
# City population is 10,000
CityPop(10000)
```

Next, we want to initialize the applied drivers stock,
and specify a constant rate of 100 people in the city applying
to become drivers each round. This will only happen until
the 10,000 potential drivers in the city are exhausted,
at which point there will be no one left to apply.

```
# 100 folks apply to become drivers per round
# the @ 100 format is called a "rate" flow
CityPop > AppliedDrivers @ 100
```

Now we want to initialize the eligible drivers stock,
and specify that 25% of the folks in applied drivers
will advance to become eligible each round.

Before we used `@ 100` to specify a fixed rate.
Here we're using `@ Leak(0.25)` to specify the idea
of 25% of the folks in applied drivers advancing into eligible driver.

```
# 25% of applied drivers become eligible each round
AppliedDrivers > EligibleDrivers @ Leak(0.25)
```
You could write this as `@ 0.25`, but you'd actually get different behavior,
That's because `@ 0.25` is actually short-hand for `@ Conversion(0.25)`,
which is similar to a leak but destroys the unconverted portion.

Using an example to show the difference, let's imagine that
we have 100 applied drivers and 100 eligible drivers, and then
see the consequences of applying a leak versus a conversion:

* `Leak(0.25)` would end with 75 applied drivers and 125 eligible drivers
* `Conversion(0.25)` would end with 0 applied drivers and 125 eligible drivers

Depending on what you are modeling, you might need leaks, conversions or both.

Moving on, next we model out first right-to-left flow.
Specifically, the request missing information flow where some eligible drivers end up
not being eligible because they need to provide more information.

```
# This is "Request missing information", with 10%
# of folks moving backwards each round
EligibleDrivers > AppliedDrivers @ Leak(0.1)
```

Note that the syntax for left-to-right and right-to-left flows
is identical, without making a distinction.

Now, 25% of eligible drivers become onboarded drivers each round.

```
# 25% of eligible drivers onboard each round
EligibleDrivers > OnboardedDrivers @ Leak(0.25)
```

Then 50% of onboarded drivers become active drivers,
actually providing rides.

```
# 50% of onboarded drivers become active
OnboardedDrivers > ActiveDrivers @ Leak(0.50)
```

The active drivers stock is drained by two flows:
drivers who voluntarily depart become departed drivers,
and drivers who are suspended become suspended drivers.
Both flows take 10% of active drivers each round.

```
# 10% of active drivers depart voluntarily and involuntarily
ActiveDrivers > DepartedDrivers @ Leak(0.10)
ActiveDrivers > SuspendedDrivers @ Leak(0.10)
```

Finally, we also see 5% of departed drivers returning to driving
each round. Similarly, we unsuspend 1% of suspended drivers.

```
# 5% of DepartedDrivers become active
DepartedDrivers > ActiveDrivers @ Leak(0.05)
# 1% of SuspendedDrivers are reactivated
SuspendedDrivers > ActiveDrivers @ Leak(0.01)
```

We already sketched this model out earlier, but it's worth noting
that `systems` will allow you to export models via [Graphviz](https://graphviz.org/).
These diagrams are generally harder to read than a custom drawn one,
but it's certainly possible to use this toolchain to combine sketching
and modeling into a single step.

![The image is a flowchart depicting the journey of drivers through various stages. It consists of six stages represented by labeled ovals connected by directional arrows indicating the process flow. 

1. **CityPop**: The starting point of the process.
2. **AppliedDrivers**: The next stage, connected by an arrow from CityPop, indicating drivers who have applied.
3. **EligibleDrivers**: Drivers who are eligible, connected by arrows to and from AppliedDrivers, suggesting potential back-and-forth or review.
4. **OnboardedDrivers**: This stage comes after eligibility, indicating drivers who have completed onboarding.
5. **ActiveDrivers**: The stage where drivers are actively participating, connected from OnboardedDrivers.
6. **DepartedDrivers and SuspendedDrivers**: Two final possible outcomes, both connected from ActiveDrivers, indicating drivers who either leave or are suspended from being active.

The flowchart provides a clear, linear progression with options for review and different end states for the drivers.](https://craftingengstrategy.com/static/blog/strategy/llm-ride-model-2.png)

<p class="img-desc i tc f6">GraphViz representation of systems model</p>

Now that we have the model, we can get to exercise it to learn its secrets.

## Exercise

Our base model acquires initial drivers quickly, then slows as city population is exhausted.

![The image is a line graph titled "ActiveDrivers Over Time." It represents the number of active drivers plotted against time.

- **X-Axis (Horizontal):** Labeled "Time" and ranges from 0 to 250.
- **Y-Axis (Vertical):** Labeled "# ActiveDrivers" and ranges from 0 to 1400.

The line begins near the origin with a steep increase in the number of active drivers, reaching a peak slightly over 1300. After peaking, there is a decline which transitions into a gradual drop, followed by stabilization at just above 600 active drivers towards the end of the time period.](https://craftingengstrategy.com/static/blog/strategy/llm-ride-results-1.png)

<p class="img-desc i tc f6">Base onboarding model stabilizing around 800 active drivers</p>

Now let's imagine that our LLM-powered tool can speed up eligible drivers, doubling the speed that we move
applied drivers to eligible drivers. Instead of 25% of applied drivers becoming eligible each round,
we'll instead see 50%.

```
# old
AppliedDrivers > EligibleDrivers @ Leak(0.25)

# new
AppliedDrivers > EligibleDrivers @ Leak(0.50)
```

Unfortunately, we can see that even doubling the speed at which we're onboarding drivers to eligible
has a minimal impact.

![The image is a line graph titled "ActiveDrivers Over Time." 

- **Axes**:
  - The x-axis is labeled "Time."
  - The y-axis is labeled "# ActiveDrivers."

- **Lines and Legend**:
  - There are two lines on the graph:
    - A blue line labeled "Base."
    - An orange line labeled "FastOnboarding."
  - The lines represent the number of active drivers over time for two scenarios.

- **Data Trends**:
  - Both lines start from the origin, indicating a similar starting point with very few active drivers.
  - Initially, the orange "FastOnboarding" line rises more steeply than the blue "Base" line, indicating a faster increase in active drivers.
  - Both lines peak around the same point in time, with the maximum number of active drivers slightly above 1300.
  - After peaking, both lines decline and then stabilize, with "FastOnboarding" slightly maintaining a higher number of active drivers compared to "Base."

Overall, the graph compares the growth and stabilization of active drivers over time between two scenarios: "Base" and "FastOnboarding".](https://craftingengstrategy.com/static/blog/strategy/llm-ride-results-2.png)

<p class="img-desc i tc f6">Speeding up onboarding doesn't impact active drivers in the long-term</p>

To finish testing this hypothesis, we can eliminate the `Request missing information` flow entirely
and see if this changes things meaningfully, commenting out that line.

![The image is a line graph titled "ActiveDrivers Over Time" that displays the number of active drivers over time for three different scenarios. The x-axis represents time, while the y-axis shows the number of active drivers, ranging from 0 to 1400.

Three lines are plotted on the graph:

1. **Blue Line (Base):** Represents the base scenario. It starts from the origin, rises steadily, peaks slightly above 1200 at around time 100, and then gradually declines and levels off past time 150.

2. **Orange Line (FastOnboarding):** Begins similarly to the blue line, but it follows a slightly higher trajectory initially, also peaking near time 100, and then follows a similar decline.

3. **Green Line (NoMissingInfo):** Starts at the same point as the others and closely follows the same path as the orange line, peaking at a similar point and declining similarly.

The lines initially converge and rise steeply, peak, and then uniformly decline and level off, suggesting different onboarding strategies' impacts on driver activity. A legend in the top right corner identifies the line colors associated with each scenario.](https://craftingengstrategy.com/static/blog/strategy/llm-ride-results-3.png)

<p class="img-desc i tc f6">Eliminating request missing information error doesn't impact active drivers long-term</p>

Unfortunately, even eliminating the missing information rate has little impact on the number of active drivers.
So it seems like the opportunity for our LLM solutions to increase active drivers are going to need to focus
on reactivating existing drivers.

Specifically, let's go from 5% of departed drivers reactivating to 20%.

```
# 20% of DepartedDrivers become active
# DepartedDrivers > ActiveDrivers @ Leak(0.05)
# DepartedDrivers > ActiveDrivers @ Leak(0.2)
```

For the first time, we're seeing a significant shift in impact.
We reach a much higher percentage of drivers at peak, and even after we
exhaust all drivers in a city, the total number of active reaches a higher
equilibrium.

![The image is a line graph titled "ActiveDrivers Over Time," showing the number of active drivers over a period. The x-axis represents time, while the y-axis represents the number of active drivers, ranging from 0 to 1600.

There are two lines on the graph:

1. **Blue Line (Base):** This line starts near the origin, increases steadily to a peak at around 1000 active drivers, then declines and stabilizes at around 800 drivers.

2. **Orange Line (LLM_Reengage):** This line also starts at a similar point, increasing to a higher peak of around 1600 drivers, then decreases and stabilizes at about 1000 drivers.

The orange line shows higher engagement throughout the period. A legend in the top-right corner identifies the lines as "Base" and "LLM_Reengage."](https://craftingengstrategy.com/static/blog/strategy/llm-ride-results-4.png)

<p class="img-desc i tc f6">Improving driver reengagement does increase active drivers</p>

Presumably increasing the rate that we reactivate suspended drivers from 1% to 2.5% would
have a similar, meaningful but smaller impact on active drivers over time.
So let's model that change.

```
# 2.5% of SuspendedDrivers are reactivated
#SuspendedDrivers > ActiveDrivers @ Leak(0.01)
SuspendedDrivers > ActiveDrivers @ Leak(0.025)
```

However, surprisingly, the impact of increasing the reactivation rate of suspended drivers is
actually much higher than reengaging departed drivers.

![The image is a line graph titled "ActiveDrivers Over Time." It shows the number of active drivers as a function of time. There are three lines representing different scenarios:

1. **Blue Line ("Base")**: This line starts from zero, gradually rises, peaks, and then declines slightly before leveling off. It represents the baseline scenario.

2. **Orange Line ("LLM_Reengage")**: This line closely follows the blue line but peaks slightly higher and later, indicating a reengagement scenario where more drivers become active.

3. **Green Line ("LLM_Unsuspend")**: This line rises steeply, peaks at a much higher number of active drivers, and then declines sharply, leveling off above the other two lines. This shows an unsuspension scenario that leads to a significant increase in active drivers.

The x-axis represents time, ranging from 0 to 250, and the y-axis represents the number of active drivers, ranging from 0 to 2500. The legend in the upper right identifies each line.](https://craftingengstrategy.com/static/blog/strategy/llm-ride-results-5.png)

<p class="img-desc i tc f6">Increasing reactivation rate of suspend drivers has highest impact</p>

This is an interesting, and somewhat counter-intuitive result.
Increasing the rate for both suspended and departed rates is more impactful
than increasing either, because ultimately there's a growing population of drivers
in the slower deflating stock.
This means, surprisingly, that a tool that helps us quickly determine which drivers
could be unsuspended might matter more than the small size of the flow indicates.

At this point, we've probably found the primary story that this model wants to tell us:
we should focus efforts on reactivating departed and suspended drivers.
Changes elsewhere might reduce operational costs of our business, but they won't
solve the problem of increasing active drivers.
````

## File: llm/26000_private-equity-takeover-strategy.md
````markdown
# Navigating Private Equity ownership.
url: https://craftingengstrategy.com/private-equity-strategy

In 2020, you could credibly argue that [ZIRP explains the world](https://www.readmargins.com/p/zirp-explains-the-world),
but that's an impossible argument to make in 2024 when zero-interest rate policy is only a fond memory.
Instead, we're seeing a number of companies designed for rapid expansion, learning to adapt
to a world that expects immediate free cash flow rather than accepting the sweet promise of discounted future cash flow.

This chapter aims to tackle that problem head-on, taking the role of an engineering organization attempting to navigate
new ownership by a private equity group. It's an increasingly frequent scenario: after many years of learning to operate under the direction of its original founders,
and the brief excitement of going public, now there's a short runway to change operating models.

Let's call this company Fungible Ecommerce Company. It's a platform for supporting online commerce,
and this is their Engineering Leadership team's attempt to think through
their options while waiting for new ownership to provide concrete guideposts.

---

*This is an exploratory, draft chapter for a book on engineering strategy that I'm brainstorming in [#eng-strategy-book](https://lethain.com/tags/eng-strategy-book/).*
*As such, some of the links go to other draft chapters, both published drafts and very early, unpublished drafts.*

## Reading this document

To apply this strategy, start at the top with _Policy_. To understand the thinking behind this strategy, read sections in reverse order, starting with _Explore_, then _Diagnose_ and so on.
Relative to the default structure, this document has been refactored in two ways
to improve readability:
first, _Operation_ has been folded into _Policy_;
second, _Refine_ has been embedded in _Diagnose_.

More detail on this structure in [Making a readable Engineering Strategy document](https://lethain.com/readable-engineering-strategy-documents).

## Policy

Our policy for managing our new ownership structure is:

* We believe our new ownership will provide a specific target for Research and Development (R&D) operating expenses
    during the upcoming financial year planning. **We will revise these policies again once we have explicit targets**,
    and will delay planning around reductions until we have those numbers to avoid running two overlapping processes.

    That said, looking at our R&D investment relative to comparably growing peer set,
    we believe that we'll get pressure to moderately reduce our spend. We aim to accomplish
    that reduction through a series of policies and one-off infrastructure projects, without requiring a major
    reduction in headcount spend.
* **We will move to an "N-1" backfill policy**, where departures are backfilled with a less senior level.
    **We will also institute a strict maximum of one Principal Engineer per business unit**, with any exceptions approved
    in writing by the CTO--this applies for both promotions and external hires.
    These policies are effective immediately, and are based on our [model of engineering-org seniority-mix](https://craftingengstrategy.com/private-equity-model/).

    We commit to this policy reducing headcount costs by approximately 5% YoY every year for the foreseeable future.
* We evaluated a number of potential changes to our geographical hiring strategy,
    but we believe that staffing engineers with cross-functional partners (Product, Marketing, Sales, and so on)
    is a priority.
    We have not been able to reach an agreement cross-functionally, and as such
    **we are not changing our geographical hiring strategy at this time**.

    If we can agree on a policy here, we could accomplish 10-20% reduction in cost over 2-3 years,
    but the details matter a great deal, so we cannot commit to a specific outcome until we get
    more cross-functional alignment.
* Our infrastructure spend has grown significantly more slowly than revenue for the past two years,
    meaning that we've successfully implemented our infrastructure spend strategy of
    [growing infrastructure costs more slowly than revenue](https://infraeng.dev/efficiency/).
    **We will continue our current infrastructure efficiency strategy**, and believe there are relatively few high impact efficiency opportunities at this point.

    We commit to growing infrastructure spend at no more than 5% YoY, significantly lower than our projected
    revenue increase of 25% YoY.
* There are two narrow infrastructure spend opportunities, both related to the integration of prior acquisitions
    into our shared infrastructure and away from one-off approaches.
    **We will prioritize the post-acquisition integration work next quarter**, with the goal of fully standardizing all infrastructure
    across the company into the stack maintained by our centralized Infrastructure Engineering team.

    We commit to a one-time reduction in infrastructure of 3% YoY.
* We believe there are significant opportunities to reduce R&D maintenance investments,
    but we don't have conviction about which particular efforts we should prioritize.
    **We will kickoff a working group to identify the features with the highest support load.**

## Diagnose

We've diagnosed Fungible Ecommerce Company's current state as:

* Fungible Ecommerce Company's revenue has grown 20-25% YoY for the past two years,
    and our target for next year is 25% YoY revenue growth.
    While this is not a guarantee, we grew slower than 25% last year, it's a defensible
    goal that we have a good chance of achieving.
* Our Engineering headcount costs have grown by 15% YoY this year, and 18% YoY the prior year.
    Headcount grew 7% and 9% respectively, with the difference between headcount and headcount costs
    explained by salary band adjustments (4%), a focus on hiring senior roles (3%), and increased hiring in higher cost geographic regions (1%).
* Based on general practice, it seems likely that our new Private Equity ownership will expect us
    to reduce R&D headcount costs through a reduction.
    However, without concrete details, we cannot yet make structured decisions.
    Our strategy will depend significantly on the scale of any proposed reductions.
* Infrastructure engineering spend (including vendors) has grown by 4-5% YoY for the past three years.
    We made a significant push on reducing costs three years ago, and have grown slower
    than revenue since then.

    There are few remaining opportunities to significantly reduce infrastructure costs,
    but we've made several acquisitions since our prior infrastructure consolidation,
    that represent significant potential savings: roughly one-time 1.5% YoY reductions for each of two largest opportunities.
* A significant portion of our current R&D spend goes into maintaining our existing functionality,
    particularly functionality related to earlier geo-expansion efforts that only apply narrowly to some small markets.
    We suspect there's an opportunity to reduce maintenance overhead here.

    However, we lack believable metrics on both (1) time spent maintaining the software
    and (2) time that would be saved by these cleanup efforts. As a result, it's hard
    to pitch projects of this sort as revenue saving with much conviction.

## Explore

Financial markets evaluate companies in comparison to their peers.
This is most obvious in public markets, where there's significant information transparency
about business performance, and sufficient liquidity to allow markets to revalue companies
in something approaching real-time. While private equity firms generally take controlling interest
of private businesses, or with the intent of taking the business private if it happens to be public,
they value businesses in the same way.

In this exploration, we're going to dig into two particular questions.
First, we're going to dig into a dataset on the performance of public technology companies,
and then second we're going to look into the concrete example of Zendesk,
[who were taken private in 2022](https://www.reuters.com/markets/deals/zendesk-goes-private-10-bln-deal-2022-11-22/)
after being bought by two private equity firms.

### Comparable companies

Exploring the benchmarking question first, most investors evaluate engineering within the context
of the overall Research & Development (R&D) investment. They generally judge that spend by constructing
a scatterplot of R&D spend versus year-over-year revenue growth for a cohort of similar companies.
Perfectly similar companies don't exist, so this cohort is generally constructed from companies in similar
industries, with similar revenue, and operating in the same regions.

We have reached out to our investors to see if they can provide the internal datasets they use for
this analysis, but in the meantime we've developed a directionally useful dataset using the
[2023 R&D Investment Scoreboard](https://iri.jrc.ec.europa.eu/scoreboard/2023-eu-industrial-rd-investment-scoreboard),
with  some [rough cutting of the data](https://docs.google.com/spreadsheets/d/1IwO3XWDd1inVXLBw4FhkaQh5OuUlYQf0NsX95nPiOtA/edit?gid=943277176#gid=943277176)
to remove outliers.
(If we repeat this process, we will use the [SEC's EDGAR database](https://www.sec.gov/search-filings) to pull
a more specifically helpful dataset, but this has been a useful starting point.)

![The image is a scatter plot chart titled “Op Profit Growth % vs R&D Spend (1,000,000 Euros).” It visualizes the relationship between year-over-year operating profit growth percentage and R&D spending in millions of euros for various companies.

**Axes:**
- The x-axis represents R&D Spend in millions of euros, ranging from $400 million to $1,600 million.
- The y-axis represents YoY Op Profit Growth %, ranging from -500% to 250%.

**Quadrants:**
1. **Top-left quadrant:** Companies with higher profitability growth and lower R&D spend, including Aurora Innovation, DoorDash, and Arista Networks.
2. **Top-right quadrant:** Companies with higher profitability growth and higher R&D spend, including Autodesk, Cadence Design Systems, and Palo Alto Networks.
3. **Bottom-left quadrant:** Companies with lower profitability growth and lower R&D spend, including Pure Storage and Take-Two Interactive Software.
4. **Bottom-right quadrant:** Companies with lower profitability growth and higher R&D spend, with examples like Activision Blizzard and Atlassian.

**Notable Points:**
- Atlassian has the highest R&D spend, positioned in the bottom-right corner.
- Aurora Innovation is one of the highest in profit growth with relatively low R&D spend.
- Several companies like ServiceNow, Synopsys, and Activision Blizzard are grouped in the top-right quadrant, indicating both high profitability growth and higher R&D investment.](https://craftingengstrategy.com/static/blog/strategy/rd-opincome-2022.png)

<p class="img-desc i tc f6">R&D investment versus operating profit growth at public companies</p>

This isn't a perfect dataset, we prefer revenue growth over growth in operating profit, but
it's the best option within the dataset that we were able to quickly pull down.
Nonetheless, there's a clear strong performer quadrant in top-left that we can plot ourselves into
to understand our general performance, which is discussed further in the diagnosis section above.

### Zendesk

The second topic of exploration we dug into is understanding the general sequence of steps taken by private
equity ownership after acquiring a company.
For an example with available public documentation, we focused on [the purchase of Zendesk in 2022](https://www.reuters.com/markets/deals/zendesk-goes-private-10-bln-deal-2022-11-22/).

To start, we pulled Zendesk's [final 10-Q before going private](https://www.sec.gov/ix?doc=/Archives/edgar/data/0001463172/000146317222000236/zen-20220630.htm).

![The image is a financial statement comparing figures for the three months and six months ending June 30 in 2022 and 2021. It includes categories such as revenue, cost of revenue, gross profit, and operating expenses. The numbers are presented in thousands of dollars and are organized into two main timeframes: three months and six months, each comparing data from 2022 and 2021. The table highlights specific areas in a light blue background, and key figures are underlined. Here's a detailed breakdown:

### Three Months Ended June 30,
- **2022**
  - **Revenue**: $407,208
  - **Cost of Revenue**: $82,790
  - **Gross Profit**: $324,418
  - **Operating Expenses**:
    - Research and Development: $110,539
    - Sales and Marketing: $209,160
    - General and Administrative: $97,210
  - **Total Operating Expenses**: $416,909
  - **Operating Loss**: $(92,491)

- **2021**
  - **Revenue**: $318,216
  - **Cost of Revenue**: $66,743
  - **Gross Profit**: $251,473
  - **Operating Expenses**:
    - Research and Development: $82,826
    - Sales and Marketing: $165,250
    - General and Administrative: $45,818](https://craftingengstrategy.com/static/blog/strategy/zendesk-pl-2022.png)

<p class="img-desc i tc f6">Zendesk's P&L from their 2022 10-Q</p>

Taking those values, we can reformat them into a chart focusing on the year-over-year
changes in the 6 months period ending in 2022 versus the same period in 2021.

![The image is a table comparing financial data between the years 2021 and 2022. It includes three columns labeled "2021," "2022," and "YoY" (Year over Year). The table shows four rows of financial metrics:

1. **Revenue:**
   - 2021: 616,264
   - 2022: 795,535
   - YoY: 29.09%

2. **R&D Expenses:**
   - 2021: 156,609
   - 2022: 218,616
   - YoY: 39.59%

3. **S&M Expenses:**
   - 2021: 322,768
   - 2022: 410,820
   - YoY: 27.28%

4. **G&A Expenses:**
   - 2021: 88,951
   - 2022: 160,748
   - YoY: 80.72%

Each row compares the respective financial figures for 2021 and 2022, along with the percentage change year over year.](https://craftingengstrategy.com/static/blog/strategy/zendesk-yoy-6m-2022.png)

<p class="img-desc i tc f6">Zendesk's P&L from their 2022 10-Q, reformatted to show year-over-year changes</p>

The changes are a bit concerning. Sales and Marketing costs have grown  more slowly than revenue, which is positive,
but Research and Development (R&D) expenses have grown about 50% faster than revenue, and General and Administration (G&A) charges
have grown more than twice as quickly as revenue.

From those growth rates, we would assume that the new ownership might push to aggressively reduce spend in those two
areas, which is indeed what history suggests happened, with a
[November, 2022 reduction](https://www.zendesk.com/newsroom/articles/company-announcement/),
followed some months later by a
[May, 2023 reduction](https://www.zendesk.com/newsroom/articles/zendesk-workforce-reduction/).
It's hard to get precise data here, but it's our impression that these reductions focused on
areas where expenses were growing quickly, with particular focus on G&A functions.
````

## File: llm/27000_eng-cost-model.md
````markdown
# Eng org seniority-mix model.
url: https://craftingengstrategy.com/private-equity-model

One of the trademarks of private equity ownership is the expectation that either the company maintains their current margin
and grows revenue at 25-30%, or they instead grow slower and increase their free cash flow year over year.
In many organizations, engineering costs have a major impact on their free cash flow.
There are many costs to reduce, cloud hosting and such, but inevitably part of the discussion is
addressing engineering headcount costs directly.

One of the largest contributors to engineering headcount costs is your organization's seniority mix:
more senior engineers are paid quite a bit more than earlier career engineers.
This model looks at how various policies impact an organization's seniority mix.

In this chapter, we'll work to:

1. Summarize this model's learnings about policy impact on seniority mix
2. Sketch the model's stocks and flows
3. Use [lethain/systems](https://github.com/lethain/systems) to iteratively build and exercise the full model

Time to start modeling.

## Learnings

An organization without a "backfill at N-1" hiring policy, e.g. an organization that hires a SWE2 to replace a departed SWE2,
will have an increasingly top-heavy organization over time.

![The image is a line graph titled "SWEs Over Time," showing the number of SWEs (Software Engineers) over a period of 50 time units. The y-axis is labeled "# SWEs," and the x-axis is labeled "Time."

The graph features four lines, each representing a different category of SWEs at the same level, as indicated by the legend:

1. Blue line: AtSameLevel SWE1, which remains relatively constant over time.
2. Orange line: AtSameLevel SWE2, which slightly increases initially and then flattens out.
3. Green line: AtSameLevel SWE3, showing a gradual increase and stabilizes towards the end.
4. Red line: AtSameLevel SWE4, displaying a significant upward trend over the entire time period, ending at around 250 on the y-axis.

The red line shows the strongest growth compared to the other lines. The graph is simple and clear, emphasizing the varying growth rates of the different categories over time.](https://craftingengstrategy.com/static/blog/strategy/eng-costs-model-2.png)

<p class="img-desc i tc f6">Ratio of engineers at senior-most level becomes increasingly heavy over time</p>

However, even introducing the "backfill at N-1" hiring policy is insufficient, as our representation
in senior levels will become far too high, even if we stop hiring externally into our senior-most levels.

![The image is a line graph titled "SWEs Over Time," which likely refers to Software Engineers. The graph shows the progression of headcount over time for four different groups. 

1. **Axes:**
   - The x-axis represents time, with ticks at intervals of 10, up to 50.
   - The y-axis represents the number of SWEs, ranging from 0 to 100.

2. **Data Series:**
   - There are four lines, each representing a different group labeled in the legend:
     - **FlatHeadcount SWE1**: Blue line, starting around 100 and decreasing rapidly to stabilize around 70.
     - **FlatHeadcount SWE2**: Orange line, starting slightly below 100, decreasing gradually, and stabilizing slightly below 80.
     - **FlatHeadcount SWE3**: Green line, starting near 100, decreasing to below 70, and then rising slightly before stabilizing.
     - **FlatHeadcount SWE4**: Red line, increasing steadily from around 15 to stabilize at 60.

3. **Trends:**
   - SWE4 is the only group showing a significant increase over time.
   - The other three groups (SWE1, SWE2, SWE3) show an initial decrease and eventual stabilization.

Overall, the graph illustrates differing trends in headcount for each group over the depicted period.](https://craftingengstrategy.com/static/blog/strategy/eng-costs-model-4.png)

<p class="img-desc i tc f6">Implementing an N-1 backfill policy prevents unbounded increase of rate of senior-most engineers</p>

To fully accomplish our goal of a healthy seniority mix, we must stop hiring at senior-most levels,
implement a "backfill at N-1" policy, and cap the maximum number of individuals at the senior-most level.

![The image is a line graph titled "SWEs Over Time." It displays the number of SWEs (Software Engineers) over a time period on the x-axis, which ranges from 0 to 50. The y-axis represents the number of SWEs, ranging from 0 to 100.

There are four lines on the graph, each representing a different SWE category:

1. **CapSWE4 SWE1 (Blue line):** Starts at around 100 SWEs and declines quickly to stabilize at around 80.
2. **CapSWE4 SWE2 (Orange line):** Begins slightly below 100 and stabilizes at around 90.
3. **CapSWE4 SWE3 (Green line):** Starts near 100 and soon stabilizes at approximately 98.
4. **CapSWE4 SWE4 (Red line):** Starts at approximately 20 and remains constant.

Each category is distinguished by a color and labeled with a legend on the right. The lines indicate that most categories start at a higher number and then stabilize, except for SWE4, which remains constant.](https://craftingengstrategy.com/static/blog/strategy/eng-costs-model-5.png)

<p class="img-desc i tc f6">N-1 backfill policy and capping number of engineers at senior-most level</p>

Any collection of lower-powered policies simply will not impact the model's outcome.

## Sketch

We'll start by sketching this system in [Excalidraw](https://excalidraw.com/).
It's always fine to use whatever tool you prefer, but simpler sketching tools
generally help you focus on iterating the stocks and flows--without getting distracted
by tuning settings--much like a designer starting with messy wireframes rather than pixel-perfect designs.

We'll start with sketching the junior-most level: SWE1.

![The image is a flowchart depicting the career progression and transition of roles within an organization. Here's a detailed description:

1. **Boxes:**
   - There are five labeled boxes in the flowchart.
   - "Candidates": Represents potential new hires.
   - "SWE1": Represents the position of Software Engineer 1.
   - "Departed SWE1": Represents a vacated Software Engineer 1 position.
   - "SWE2": Represents the position of Software Engineer 2.

2. **Arrows and Labels:**
   - An arrow labeled "Hire" points from "Candidates" to "SWE1," indicating the recruitment process.
   - An arrow labeled "Promote" points from "SWE1" to "SWE2," indicating career advancement.
   - Two arrows labeled "Depart" and "Backfill" connect "SWE1" and "Departed SWE1." "Depart" leads from "SWE1" to "Departed SWE1," indicating someone leaving the position, and "Backfill" goes in the opposite direction, indicating filling the vacant position.

This flowchart outlines a simple workflow of hiring, promotion, and position backfilling for software engineering roles.](https://craftingengstrategy.com/static/blog/strategy/eng-costs-sketch-1.png)

<p class="img-desc i tc f6">Hiring, departures and promotions for SWE1 engineers</p>

We hire external candidates to become SWE1s. We have some get promoted to SWE2, some depart, and then backfill those
departures with new SWE1s.

![The image is a flowchart illustrating the process of hiring, promoting, departing, and backfilling positions within a hypothetical software engineering team. Here's a detailed description:

1. **Candidates**: This is the starting point where potential hires are sourced.

2. **SWE1 (Software Engineer 1)**:
   - **Hire**: Candidates are hired into the SWE1 position.
   - **Depart**: When SWE1 departs, they move to the "Departed SWE1" box.
   - **Backfill**: Vacant SWE1 positions can be filled back from Candidates.
   - **Promote**: SWE1s can be promoted to SWE2.  

3. **Departed SWE1**: This is where the SWE1s who have left are recorded.

4. **SWE2 (Software Engineer 2)**:
   - Post-promotion, SWE1s move into this role.
   - **Depart**: When an SWE2 departs, they move to the "Departed SWE2" box.
   - **Backfill at level**: SWE2 positions are backfilled from within or external candidates.
   - **Hire**: Direct hires at the SWE2 level from the Candidates pool.

5. **Departed SWE2**: This is where the SWE2s who have departed are recorded.

6. **Arrows and Labels**: 
   - Show the progression through hiring, promoting, departing, and backfilling](https://craftingengstrategy.com/static/blog/strategy/eng-costs-sketch-2.png)

<p class="img-desc i tc f6">Hiring and promotion lifecycle for SWE1 and SWE2</p>

As we start sketching the full stocks and flows for SWE2, we also introduce the idea of backfilling
at the prior level. As we replicate this pattern for two more career levels--SWE3 and SWE4--we get the
complete model.

![The image is a flowchart illustrating the hiring and promotion process for software engineers (SWE) through different levels (SWE1 to SWE4). Here's a detailed description:

1. **Candidates Pool**: At the left, there's a box labeled "Candidates" from which new hires are sourced.

2. **Hiring and Promotion**:
   - Candidates can be hired into any of the levels: SWE1, SWE2, SWE3, and SWE4.
   - Each level has a promotion path to the next higher level (e.g., SWE1 can be promoted to SWE2).

3. **Departure and Backfill**:
   - Each level (SWE1, SWE2, SWE3, SWE4) has an arrow indicating the possibility of departure leading to a "Departed SWE" state (e.g., SWE1 to Departed SWE1).
   - Departures trigger a “Backfill at level” action to fill the vacancy at the same level or a “Backfill at N-1 level” action for filling at the previous lower level.

4. **Flow**:
   - The flow is cyclic and connected, showing continuous hiring, promotion, and backfill processes.

The chart effectively maps out the movement of personnel through hiring, promotion, departure, and backfilling across different software engineering levels.](https://craftingengstrategy.com/static/blog/strategy/eng-costs-sketch-4.png)

<p class="img-desc i tc f6">Hiring and promotion lifecycle for four levels of career ladder</p>

The final level, SWE4, is simplified relative to the prior levels, as it's no longer possible to get promoted to
a further level.
We could go further than this, but the model will simply get increasingly burdensome to work with,
so let's stop with four levels.

## Reason

When reviewing the sketched system, a few interesting conclusions emerge:

1. If promotion rates at any level exceed the rate of hiring at that level plus rate of N-1 backfill at that level,
    then the proportion of engineers at that level will grow over time
2. If you are not hiring much, then this problem simplifies to promotion rate versus departure rate.
    A company that does little hiring and has high retention cannot afford to promote frequently.
    Promotion into senior roles will become financially restrained, even if the policy is explained
    by some other mechanism
3. Many companies use the "[career level](https://lethain.com/career-levels-and-more/)" policy as the mechanism
    to identify a level where promotions _generally_ stop happening. 
    The rationale is often not explicitly described, but we can conclude it's likely a financial constraint
    that typically incentivizes this policy

With those starter insights, now we can get into modeling the details.

## Model & Exercise

We're going to build this model using [lethain/systems](https://github.com/lethain/systems).
The first version will be relatively simple, albeit with a number of stocks given the size
of the model, and then we'll layer on a number of additional features as we iteratively test
out a number of different scenarios.

I've chosen to combine the Model and Exercise steps to showcase how each version of the model
can inspire new learnings that prompt new questions, that require a new model to answer.

If you'd rather view the full model and visualizations, each iteration
is [available on github](https://github.com/lethain/eng-strategy-models/blob/main/BackfillPolicy.ipynb).

## Backfill-at-level

The first policy we're going to explore is backfilling a departure at the same level.
For example, if a SWE2 departs, then you go ahead and backfill them at SWE2. This intuitively
makes sense, because you needed a SWE2 before to perform the work, so why would you hire something
less senior?

There are two new `systems` concepts introduced in this model:

1. For easier iteration, we're going to use the systems modeling concept
    of an "information link", which is basically using a stock as a variable to define a flow,
    Specifically, we'll create a stock named `HiringRate` with a size of two.
    Then we'll use that stock's size to define hiring flows at each career level.
    In programming terms, you can think as defining a reusable variable,
    but you can use any stock's size to define flows.
2. There are effectively an infinite number of potential candidates for your company,
    so we're going to use an infinite stock, represented by initializing a new stock
    surrounded by `[` and `]`. Specifically in this case this is `[Candidates]`,
    if we wanted a fixed size stock with 100 people in it, we could have initialized it as `Candidates(100)`.
    Depending on what you're modeling both options are useful.

With those in mind, our initial model is defined as:

```
HiringRate(2)

[Candidates] > SWE1(10) @ HiringRate
SWE1 > DepartedSWE1 @ Leak(0.1)
DepartedSWE1 > SWE1 @ Leak(0.5)

Candidates > SWE2(10) @ HiringRate
SWE1 > SWE2 @ Leak(0.1)
SWE2 > DepartedSWE2 @ Leak(0.1)
DepartedSWE2 > SWE2 @ Leak(0.5)

Candidates > SWE3(10) @ HiringRate
SWE2 > SWE3 @ Leak(0.1)
SWE3 > DepartedSWE3 @ Leak(0.1)
DepartedSWE3 > SWE3 @ Leak(0.5)

Candidates > SWE4(0)  @ HiringRate
SWE3 > SWE4 @ Leak(0.1)
SWE4 > DepartedSWE4 @ Leak(0.1)
DepartedSWE4 > SWE4 @ Leak(0.5)
```

To confirm that we've done something reasonable, we can model this using Graphviz.

![The image is a directed flowchart, likely representing a process related to hiring and employee turnover within a software engineering context. It includes several key components:

1. **Nodes**:
   - **Candidates**: An oval node that serves as a starting point for the flow.
   - **HiringRate**: Another oval node connected to candidates.
   - **SWE1, SWE2, SWE3, SWE4**: A series of oval nodes representing different levels or stages of software engineers.
   - **DepartedSWE1, DepartedSWE2, DepartedSWE3, DepartedSWE4**: Oval nodes indicating the departure of software engineers at various stages.

2. **Arrows (Edges)**:
   - The arrows indicate the flow or transition from one stage or node to another.
   - From **Candidates**, arrows point towards **SWE1**, **SWE2**, **SWE3**, and **SWE4**.
   - Arrows from **SWE1**, **SWE2**, **SWE3**, and **SWE4** point towards their respective departed nodes, such as **DepartedSWE1** and so on.
   - Additional transitions occur among the intermediate SWE nodes and towards higher levels.

This flowchart likely models the hiring, progression, and departure process of software engineers in an organization.](https://craftingengstrategy.com/static/blog/strategy/eng-costs-model-1.png)

<p class="img-desc i tc f6">GraphViz representation of systems model</p>

That looks like the same model we sketched before, without the downlevel backfill flows
that we haven't yet added to the model, so we're in a good spot.

With that confirmed, let's inspect the four distinct flows happening for the SWE2 stock.
In order they are:

1. External candidates being hired at the SWE2 level, at the fixed `HiringRate`
    defined here as 2 hires per round
2. SWE1s being promoted to SWE2 at a 10% rate. This is a leak because someone being promoted
    to SWE2 doesn't mean the other SWE1s disappear
3. SWE2s who are leaving the company at a 10% rate
4. Backfill hires of departed SWE2s, who are rehired at the same level

Running that model, we can see how the populations of the various levels grow over time.

![The image is a line graph titled "SWEs Over Time." It displays the development of four software engineering entities (SWEs) over a period of time, represented on the x-axis. The y-axis shows the number of SWEs.

- The blue line represents "AtSameLevel SWE1" and remains mostly constant over time.
- The orange line represents "AtSameLevel SWE2" and shows a slight increase initially before leveling off.
- The green line represents "AtSameLevel SWE3" and increases gradually before leveling off.
- The red line represents "AtSameLevel SWE4" and shows a steep, continuous increase over time.

The legend identifies the lines by color and their respective SWE identifiers. Overall, SWE4 shows the most significant growth, while the others have minimal changes.](https://craftingengstrategy.com/static/blog/strategy/eng-costs-model-2.png)

<p class="img-desc i tc f6">Ratio of engineers at senior-most level becomes increasingly heavy over time</p>

Alright, so we can tell that this backfill at level policy is pretty inefficient, because our organization
just becomes more and more top-heavy with SWE4s over time. Something needs to change.

## Backfill at N-1

To reduce the number of SWE4s in our company, let's update the model to backfill all hires at the level
below the departed employee. For example, a departing SWE2 would cause hiring a SWE1.
This specifically means replacing all these lines:

```
DepartedSWE2 > SWE2 @ Leak(0.5)
```

To instead hire into the prior level.

```
DepartedSWE2 > SWE1 @ Leak(0.5)
```

The one exception is that SWE1s are still backfilled as SWE1s: as it's the junior-most level,
there's no lower level to backfill into.

Running this updated model, we get a better looking organization.

![The image is a line graph titled "SWEs Over Time," displaying the number of SWEs on the y-axis and time on the x-axis. There are four lines, each representing different datasets:

1. **BackfillIN-1 SWE1** (blue line)
2. **BackfillIN-1 SWE2** (orange line)
3. **BackfillIN-1 SWE3** (green line)
4. **BackfillIN-1 SWE4** (red line)

The x-axis ranges from 0 to 50, while the y-axis ranges from 0 to 100. All the lines exhibit an upward trend, indicating an increase in the number of SWEs over time. The red line (BackfillIN-1 SWE4) consistently trends above the others, suggesting a higher number of SWEs compared to the other datasets. The blue line (BackfillIN-1 SWE1) remains the lowest throughout most of the timeline. The legend at the top center provides clarification for each line’s corresponding dataset.](https://craftingengstrategy.com/static/blog/strategy/eng-costs-model-3.png)

<p class="img-desc i tc f6">N-1 backfill policy without overall hiring cap</p>

We're still top-heavy, but we've turned an exponential growth problem into a linear growth problem,
so that's an improvement. However, this is still a very expensive engineering organization to run,
and certainly _not_ an organization that's reducing costs.

## No hiring

One reason our model shows so many SWE4s is because we're hiring at an even rate across all levels,
which isn't particularly realistic. Also, it's unlikely that we're growing headcount at all to the extent
that we're aiming to reduce our engineering costs over time.

We can model this by setting a `HiringRate` of zero, and then setting more representative initial
values for each cohort of engineers (note that I'm only showing the changed lines,
check [on github](https://github.com/lethain/eng-strategy-models/blob/main/BackfillPolicy.ipynb)
for the full model):

```
HiringRate(0)

[Candidates] > SWE1(100) @ HiringRate
Candidates > SWE2(100) @ HiringRate
Candidates > SWE3(100) @ HiringRate
Candidates > SWE4(10)  @ HiringRate
```

Now we're starting out with 100 SWE1s, SWE2, and SWE3s.
We have a smaller cohort of SWE4s, with just ten initially.
Running the model gives us a updated perspective.

![The image is a line graph titled "SWEs Over Time," illustrating the change in the number of Software Engineers (SWEs) over time across four scenarios, labeled as FlatHeadcount SWE1, SWE2, SWE3, and SWE4. 

**Axes:**
- The x-axis is labeled "Time" and ranges from 0 to 50.
- The y-axis is labeled "# SWEs" and ranges from 0 to 100.

**Lines:**
1. **FlatHeadcount SWE1** (blue line)
   - Starts at 100 SWEs, declines sharply initially, levels off around 65 by the end.
   
2. **FlatHeadcount SWE2** (orange line)
   - Also begins at 100, declines steadily, and stabilizes at around 80 by the end.
   
3. **FlatHeadcount SWE3** (green line)
   - Begins similarly at 100, declines rapidly, and stabilizes just below 70.
   
4. **FlatHeadcount SWE4** (red line)
   - Starts near 0, increases steadily and plateau at around 50 SWEs.

**Legend:**
- Located in the upper right corner indicating the color associated with each scenario.

The graph illustrates variations in trends for each scenario, with some lines showing a decline and stabilization, while others show growth.](https://craftingengstrategy.com/static/blog/strategy/eng-costs-model-4.png)

<p class="img-desc i tc f6">Implementing an N-1 backfill policy prevents unbounded increase of rate of senior-most engineers</p>

We can see that eliminating hiring _improves_ the ratio of SWE4s to the other levels, but it's still just too
high. We're ending up with roughly 1.25 SWE1s for each SWE4, when the ratio should be closer to five to one.

## Capped size of SWE4s

Finally, we're going to introduce a stock with a maximum size. No matter what flows _want_ to accomplish,
they cannot grow a flow over that maximum. In this case, we're defining `SWE4` as a stock with an initial
size of 10, and a maximum size of 20.

```
SWE4(10, 20)
Candidates > SWE4  @ HiringRate
```

This could also be combined into a one-liner, although it's potentially easy to miss in that case:

```
Candidates > SWE4(10, 20)  @ HiringRate
```

With that one change, we're getting close to an engineering organization that works how we want.

![The graph titled "SWEs Over Time" is a line chart depicting the number of SWEs over time for four different categories labeled as "CapSWE4 SWE1", "CapSWE4 SWE2", "CapSWE4 SWE3", and "CapSWE4 SWE4". The x-axis represents "Time" with a range from 0 to just over 50, and the y-axis represents the "# SWEs" with a range from 0 to 100.

- The blue line (CapSWE4 SWE1) starts at the top and decreases steeply, then levels off above 80.
- The orange line (CapSWE4 SWE2) follows a similar pattern starting slightly lower, decreasing, and then leveling off below the green line.
- The green line (CapSWE4 SWE3) starts at 100, drops briefly, and then levels off above 80, generally higher than the other two lines.
- The red line (CapSWE4 SWE4) starts low and quickly levels off at around 20.

The legend on the right describes the color and label of each line.](https://craftingengstrategy.com/static/blog/strategy/eng-costs-model-5.png)

<p class="img-desc i tc f6">N-1 backfill policy and capping number of engineers at senior-most level</p>

The ratio of SWE4s to other functions is right, although we can see that the backpressure means that we have
a surplus of SWE3s in this organization. You could imagine other policy work that might improve that as well,
e.g. presumably more SWE3s depart than SWE2s, because the SWE3s see their ability to be promoted is capped by
the departure rate of existing SWE4s. However, I think we've already learned quite a bit from this model,
so I'm going to end modeling here.
````

## File: llm/28000_customer-data-access-strategy.md
````markdown
# How should we control access to user data?
url: https://craftingengstrategy.com/user-data-strategy

At some point in a startup's lifecycle, they decide that they
need to be ready to go public in 18 months, and a flurry of IPO-readiness
activity kicks off.
This strategy focuses on a company working on IPO readiness,
which has identified a gap in internal controls for managing user data access.
It's a company that _wants_ to meaningfully
improve their security posture around user data access, but which has
had a number of failed security initiatives over the years.

Most of those initiatives have failed because they significantly
degraded internal workflows for teams like customer support,
such that the initial progress was reverted and subverted over time,
to little long-term effect.
This strategy represents the Chief Information Security Officer's (CISO) attempt to acknowledge and overcome those historical
challenges while meeting their IPO readiness obligations, and--most importantly--doing
right by their users.

## Reading this document

To apply this strategy, start at the top with _Policy_. To understand the thinking behind this strategy, read sections in reverse order, starting with _Explore_, then _Diagnose_ and so on.
Relative to the default structure, this document has been refactored in two ways
to improve readability:
first, _Operation_ has been folded into _Policy_;
second, _Refine_ has been embedded in _Diagnose_.

More detail on this structure in [Making a readable Engineering Strategy document](https://lethain.com/readable-engineering-strategy-documents).

## Policy & Operations

Our new policies, and the mechanisms to operate them are:

* **Controls for accessing user data must be significantly stronger prior to our IPO.**
    Senior leadership, legal, compliance and security have decided that we are not comfortable accepting the status quo
    of our user data access controls as a public company.
    We must meaningfully improve the quality of resource-level access controls
    (e.g. how we determine which rows, rather than tables, a user has permission to access)
    as part of our pre-IPO readiness efforts.
    
    Our Security team is accountable for the exact mechanisms and approach to addressing this risk.
* **We will continue to prioritize a hybrid solution to resource-access controls.**
    This has been our approach thus far, and the fastest available option.
* **Directly expose the log of our resource-level accesses to our users.**
    We will build towards a user-accessible log of all company accesses of user data,
    and ensure we are comfortable explaining each and every access.
    In addition, it means that each rationale for access must be comprehensible and reasonable
    from a user perspective.

    This is important because it aligns our approach with our users' perspectives.
    They will be able to evaluate how we access their data, and make decisions about
    continuing to use our product based on whether they agree with our use.
* **Good security discussions don't frame decisions as a compromise between security and usability.**
    We will pursue [multi-dimensional tradeoffs](https://lethain.com/multi-dimensional-tradeoffs/) to simultaneously improve security and efficiency.
    Whenever we frame a discussion on trading off between security and utility,
    it's a sign that we are having the wrong discussion, and that we should rethink our approach.

    We will prioritize mechanisms that can both automatically authorize _and_ document the rationale
    for accesses to customer data. The most obvious example
    of this is automatically granting access to a customer support agent for users who have an open support ticket
    assigned to that agent. (And removing that access when that ticket is reassigned or resolved.)
* **Measure progress on percentage of customer data access requests justified by a user-comprehensible, automated rationale.**
    This will anchor our approach on simultaneously improving the security of user data and the usability of our colleagues' internal tools.
    If we only expand requirements for accessing customer data, we won't view this as progress because it's
    not automated (and consequently is likely to encourage workarounds as teams try to solve problems quickly).
    Similarly, if we only improve usability, charts won't represent this as progress, because we won't
    have increased the number of supported requests.

    As part of this effort, we will create a private channel where the security and compliance
    team has visibility into all manual rationales for user data access, and will
    notify the manager of anyone who repeatedly uses a manual justification
    for accessing user data.
* **Expire unused roles to move towards principle of least privilege.**
    Today we have a number of roles granted in our role-based access control (RBAC) system
    to users who do not use the granted permissions.
    To address that issue, we will automatically remove roles from colleagues after 90 days of not using the role's permissions.
    
    Engineers in an active on-call rotation are the exception to this automated permission pruning.
* **Weekly reviews until we see progress; monthly access reviews in perpetuity.**
    Starting now, there will be a weekly sync between the security engineering team,
    teams working on customer data access initiatives, and the CISO. This meeting will
    focus on rapid iteration and problem solving.

    This is explicitly a forum for ongoing [strategy testing](https://craftingengstrategy.com/strategy-testing/),
    with the CISO serving as the meeting's sponsor, and their Principal Security Engineer serving as the
    meeting's guide.
    It will continue until we have clarity
    on the path to 100% coverage of user-comprehensible, automated rationales for access to customer data.

    Separately, we are also starting a monthly review of sampled accesses to customer data to ensure
    the proper usage and function of the rationale-creation mechanisms we build.
    This meeting's goal is to review access rationales for quality and appropriateness,
    both by reviewing sampled rationales in the short-term, and identifying more automated mechanisms
    for identifying high-risk accesses to review in the future.
* **Exceptions must be granted in writing by CISO.**
    While our overarching Engineering Strategy states that we follow
    an advisory architecture process as described in _[Facilitating Software Architecture](https://www.amazon.com/Facilitating-Software-Architecture-Empowering-Architectural-ebook/dp/B0DMHGWCPN/)_,
    the customer data access policy is an exception and must be explicitly approved, with documentation,
    by the CISO. Start that process in the `#ciso` channel.

## Diagnose

* We have a strong baseline of role-based access controls (RBAC) and audit logging.
    However, we have limited mechanisms for ensuring assigned roles follow
    the [principle of least privilege](https://en.wikipedia.org/wiki/Principle_of_least_privilege).
    This is particularly true in cases where individuals change teams or roles over the course
    of their tenure at the company: some individuals have collected numerous unused roles
    over five-plus years at the company.
    
    Similarly, our audit logs are durable and pervasive, but we have limited proactive mechanisms
    for identifying anomalous usage. Instead they are typically used to understand what occurred after
    an incident is identified by other mechanisms.
* For resource-level access controls, we rely on a hybrid approach between a 3rd-party platform
    for incoming user requests, and approval mechanisms within our own product.
    Providing a rationale for access across these two systems requires manual work,
    and those rationales are later manually reviewed for appropriateness in a batch fashion.
    
    There are two major ongoing problems with our current approach to resource-level access controls.
    First, the teams making requests view them as a burdensome obligation without much benefit to
    them or on behalf of the user.
    Second, because the rationale review steps are manual, there is no verifiable evidence of the quality
    of the review.
* We've found no evidence of misuse of user data.
    When colleagues do access user data, we have uniformly and consistently found that there
    is a clear, and reasonable rationale for that access. For example, a ticket in the user
    support system where the user has raised an issue.
    
    However, the quality of our documented rationales is consistently low because it depends on
    busy people manually copying over significant information many times a day.
    Because the rationales are of low quality, the verification of these rationales is somewhat arbitrary.
    From a literal compliance perspective, we do provide rationales and auditing of these rationales, but
    it's unclear if the majority of these audits increase the security of our users' data.
* Historically, we've made significant security investments that caused temporary spikes in our security posture.
    However, looking at those initiatives a year later, in many cases we see a pattern of increased scrutiny,
    followed by a gradual repeal or avoidance of the new mechanisms.
    
    We have found that most of them involved increased friction for
    essential work performed by other internal teams. In the natural order of performing work, those teams
    would subtly subvert the improvements because it interfered with their immediate goals
    (e.g. supporting customer requests).
* As such, we have high conviction from our track record that our historical approach can
    create optical wins internally. We have limited conviction that it can create long-term
    improvements outside of significant, unlikely internal changes (e.g. colleagues are markedly
    less busy a year from now than they are today).
    It seems likely we need a new approach to meaningfully shift our stance on these kinds of problems.

## Explore

Our experience is that best practices around managing internal access to user data
are [widely available through our networks](https://craftingengstrategy.com/explore/),
and otherwise hard to find. The exact rationale for this is hard to determine,
but it seems possible that it's a topic that folks are generally uncomfortable
discussing in public on account of potential future liability and compliance
issues.

In our exploration, we found two standardized dimensions (role-based access controls, audit logs),
and one highly divergent dimension (resource-specific access controls):

* **Role-based access controls** (RBAC) are a highly standardized approach at this point.
    The core premise is that users are mapped to one or more roles, and each role
    is granted a certain set of permissions. For example, a role representing the customer support agent
    might be granted permission to deactivate an account, whereas a role representing the sales engineer might be able
    to configure a new account.
* **Audit logs** are similarly standardized. All access and mutation of resources should be
    tied in a durable log to the human who performed the action. These logs should be
    accumulated in a centralized, queryable solution.

    One of the core challenges is determining how to utilize these logs proactively
    to detect issues rather than reactively when an issue has already been flagged.
* **Resource-level access controls** are significantly less standardized than RBAC
    or audit logs. We found three distinct patterns adopted by companies, with
    little consistency across companies on which is adopted.

Those three patterns for resource-level access control were:

1. **3rd-party enrichment** where access to resources is managed in a 3rd-party system
    such as Zendesk.
    This requires enriching objects within those systems with data and metadata from
    the product(s) where those objects live.
    It also requires implementing actions on the platform, such as archiving or configuration,
    allowing them to live entirely in that platform's permission structure.

    The downside of this approach is tight coupling with the platform vendor,
    any limitations inherent to that platform, and the overhead of maintaining
    engineering teams familiar with both your internal technology stack and the
    platform vendor's technology stack.
2. **1st-party tool implementation** where all activity, including creation and management of user issues,
    is managed within the core product itself. This pattern is most common in earlier stage companies
    or companies whose customer support leadership "grew up" within the organization without much
    exposure to the approach taken by peer companies.
    
    The advantage of this approach is that there is a single, tightly integrated
    and infinitely extensible platform for managing interactions.
    The downside is that you have to build and maintain all of that work internally
    rather than pushing it to a vendor that ought to be able to invest more heavily
    into their tooling.
3. **Hybrid solutions** where a 3rd-party platform is used for most actions,
    and is also used to permit resource-level access within the 1st-party system.
    For example, you might be able to access a user's data only while there is an open
    ticket created by that user, and assigned to you, in the 3rd-party platform.

    The advantage of this approach is that it allows supporting complex workflows
    that don't fit within the platform's limitations, and allows you to avoid complex coupling
    between your product and the vendor platform.

Generally, our experience is that all companies implement RBAC, audit logs, and one of the resource-level access control mechanisms.
Most companies pursue either 3rd-party enrichment with a sizable, long-standing team owning the platform implementation,
or rely on a hybrid solution where they are able to avoid a long-standing dedicated team by lumping that work into existing teams.
````

## File: llm/28500_strategy-decompose-monolith.md
````markdown
# Should we decompose our monolith?
url: https://craftingengstrategy.com/monolith-decomposition-strategy

From their [first introduction in 2005](https://en.wikipedia.org/wiki/Microservices), the debate between adopting
a microservices architecture, a monolithic service architecture, or a hybrid between the two has become one of the
least-reversible decisions that most engineering organizations make.
Even migrating to a different database technology is _generally_ a less expensive change than moving from monolith
to microservices or from microservices to monolith.

The industry has in many ways gone full circle on that debate, from most hyperscalers in the 2010s partaking in
a multi-year monolith to microservices migration, to
[Kelsey Hightower's iconic tweet on the perils of distributed monoliths](https://x.com/kelseyhightower/status/940259898331238402):

> 2020 prediction: Monolithic applications will be back in style after people discover the drawbacks of distributed monolithic applications.
> \- @KelseyHightower

Even as popular sentiment has generally turned away from microservices, many engineering organizations have a bit of both,
often the remnants of one or more earlier but incomplete migration efforts. This strategy looks at a theoretical
organization stuck with a bit of both approaches, let's call it Theoretical Compliance Company,  which is looking to determine its path forward.

Here is Theoretical Compliance Company's service architecture strategy.

---

*This is an exploratory, draft chapter for a book on engineering strategy that I'm brainstorming in [#eng-strategy-book](https://lethain.com/tags/eng-strategy-book/).*
*As such, some of the links go to other draft chapters, both published drafts and very early, unpublished drafts.*

## Reading this document

To apply this strategy, start at the top with _Policy_. To understand the thinking behind this strategy, read sections in reverse order, starting with _Explore_, then _Diagnose_ and so on.
Relative to the default structure, this document has been refactored in two ways
to improve readability:
first, _Operation_ has been folded into _Policy_;
second, _Refine_ has been embedded in _Diagnose_.

More detail on this structure in [Making a readable Engineering Strategy document](https://lethain.com/readable-engineering-strategy-documents).

## Policy

Our policy for service architecture is documented here.
All exceptions to this policy **must** escalate _to_ a local Staff-plus engineer for their
approval, and then escalate _with_ that Staff-plus engineer to the CTO.
If you have questions about the policies, ask in `#eng-strategy`.

Our policy is:

1. **Business units should always operate in their own code repository and monolith.**
    They should not provision many different services. They should rarely work in other business units' monoliths.
    There will be nuanced cases; in these cases, prefer decisions that move us closer to this policy.
2. **New integrations across business unit monoliths should be done using gRPC.**
    The emphasis here is on _new_ integrations;
    it's desirable but not urgent to migrate existing integrations that use other implementations (HTTP/JSON, etc).

    When the decision is subtle (e.g. changes to an existing endpoint), optimize for
    business velocity rather than technical purity. When the decision is far from subtle (e.g. brand new endpoint),
    comply with the policy.
3. **Except for new business unit monoliths, we don't allow new services.**
    You should work within the most appropriate business unit monolith or within the existing infrastructure repositories.
    Provisioning a new service, unless it corresponds with a new business unit, always
    requires approval from the CTO in `#eng-strategy`.

    That approval generally will *not* be granted, unless
    the new service requires significantly different non-functional requirements than an existing monolith.
    For example, if it requires significantly higher compliance review prior to changes such as our existing
    payments service, or if it requires radically higher requests per second, and so on.
4. **Merge existing services into business-unit monoliths where you can.**
    We believe that each choice to move existing services back into a monolith should
    be made "in the details" rather than from a top-down strategy perspective. Consequently,
    we generally encourage teams to wind down their existing services outside of their business unit's monolith,
    but defer to teams to make the right decision for their local context.

## Diagnose

Theoretical Compliance Company has a complex history with decomposing our monolith.
We are also increasing our number of business units, while limiting our investment into
our core business unit. These are complex times, with a lot of constraints to juggle.
To improve readability, we've split the diagnosis into
two sections: "business constraints" and "engineering constraints."

Our business constraints are:

1. We sell business-to-business compliance solutions to other companies on an annual subscription.
    There is one major, established business line, and two smaller partially validated business lines
    that are intended to attach to the established business line to increase average contract value.
2. There are 2,000 people at the company. About 500 of those are in the engineering organization.
    Within that 500, about 150 work on the broadest definition of "infrastructure engineering,"
    things like developer tools, compute and orchestration, networking, security engineering, and so on.
3. The business is profitable, but revenue growth has been 10-20% YoY, creating persistent pressure on spend
    from our board, based on mild underperformance relative to public market comparables.
    **Unless we can increase YoY growth by 5-10%, they expect us to improve free cash flow by 5-10% each year**,
    which jeopardizes our ability to maintain long-term infrastructure investments.
4. **Growth in the primary business line is shrinking.**
    The company's strategy includes spinning up more adjacent business units to increase average contract value with new products.
    **We need to fund these business units without increasing our overall budget**,
    which means budget for the new business units must be pulled away from either our core business or our platform teams.
    
    In addition to needing to fund our new business units, **there's ongoing pressure to make our core business more efficient**,
    which means either accelerating growth or reducing investment. It's challenging to accelerate growth while reducing investment,
    which suggests that most improvement will come from reducing our investment
5. Our methodology to allocate platform costs against business units does so proportionately to
    the revenue created by each business unit. **Our core business generates the majority of our revenue, which means it is accountable for the majority of our platform costs**,
    even if those costs are motivated by new business lines.
    
    This means that, even as the burden placed on platform teams increases due to spinning up multiple business units,
    there's significant financial pressure to reduce our platform spend because it's primarily represented as a cost to the core business
    whose efficiency we have to improve.
    This means we have little tolerance for anything that increases infrastructure overhead.

Our engineering constraints are:

1. Our infrastructure engineering team is 150 engineers supporting 350 product engineers,
    and it's certain that **infrastructure will not grow significantly in the foreseeable future**.
2. We spun up two new business units in the past six months, and **plan to spin up an additional two new business units**
    in the next year. Each business unit is led by a general manager, with engineering and product within that business unit
    principally accountable to that general manager. Our CTO and CPO still set practice standards, but it's situationally-specific
    whether these practice standards or direction from general manager is the last word on any given debate.

    For example, one business unit has been unwilling to support an on-call rotation for their product, because their general
    manager insists it is a wasteful practice. Consequently, that team often doesn't respond to pages, even when their service
    is responsible for impacting the stability of shared functionality.
3. We've modeled [how services and monoliths create overhead for both product and infrastructure organizations over time](https://lethain.com/services-overhead-model/),
    and have conviction that, in general, **it's more overhead for infrastructure to support more services**.
    We also found that in our organization, the rate of service ownership changing due to team reorganizations counteracts much of the initial productivity
    gains from leaving the monolith.
4. There is some tension between the two preceding observations: it's generally more overhead to have more services,
    but it's _even more_ overhead to have irresponsible business units breaking a shared monolithic service.
    For example, we can much more easily rate limit usage from a misbehaving service than fix a misbehaving codepath
    within a shared service.
5. We also have a payments service that moves money from customers to us.
    **Our compliance and security requirements for changes to this service are significantly higher**
    than for the majority of our software, because the blast radius is essentially infinite.
6. Our primary programming language is Ruby, which generally relies on blocking IO,
    and service-oriented architectures generally spend more time on blocking IO than monoliths.
    Similarly, Ruby is _relatively_ inefficient at serializing and deserializing JSON payloads,
    which our service architecture requires as part of cross-service communication.
7. We've previously attempted to decompose, and have **a number of lingering partial migrations that don't align cleanly with our current business unit ownership structure**.
    The number of these new services continues to grow over time,
    creating more burden on both infrastructure today and product teams in the future as they try to 
    maintain these services through various team reorganizations.

## Explore

In the late 2010s, most large or scaling companies adopted services to some extent.
Few adopted microservices, with the majority of adopters opting for a [service-oriented architecture](https://aws.amazon.com/compare/the-difference-between-soa-microservices/) instead.
[Kelsey Hightower's iconic tweet on the perils of distributed monoliths](https://x.com/kelseyhightower/status/940259898331238402) in 2020
captured the beginning of a reversal, with more companies recognizing the burden of operating service-oriented architectures.

In addition to the wider recognition of those burdens, many of the cloud infrastructure challenges that originally motivated service architectures began
to mellow. Most infrastructure engineers today _only_ know how to operate with cloud-native patterns, rather than starting from machine oriented approaches.
Standard database technologies like PostgreSQL have significantly improved capabilities. Cloud providers have fast local caches for quickly retrieving verified upstream packages.
Supply and cost of cloud compute is affordable. Slow programming languages are faster than they were a decade ago. Untyped languages have reasonable incremental paths
to typed codebases.

As a result of this shift, if you look at a new, emerging company,  it's particularly likely to have a monolith in one backend and one frontend programming language.
However, if you look at a five-plus-year-old company, you might find almost anything. One particularly common case is a monolith with most functionality,
and an inconsistent constellation of team-scoped macroservices scattered across the organization.

The shift away from [zero interest-rate policy](https://en.wikipedia.org/wiki/Zero_interest-rate_policy) has also impacted trends,
as service-oriented architectures tend to require more infrastructure to operate efficiently, such as service meshes, service provisioning and deprovisioning, etc.
Properly tuned, service-oriented architectures ought to be cost competitive, and potentially superior in complex workloads, but it's
hard to maintain the required investment in infrastructure teams when in a cost-cutting environment.
This has encouraged new companies to restrict themselves to monolithic approaches, and pushed existing companies to
_attempt_ to reverse their efforts to decompose their prior monoliths, with mixed results.
````

## File: llm/29000_calm-product-eng-company.md
````markdown
# "We're a product engineering company!" — Engineering strategy at Calm.
url: https://craftingengstrategy.com/product-eng-strategy

In my career, the majority of the strategy work I've done has been in non-executive roles,
things like [Uber's service migration](https://craftingengstrategy.com/uber-strategy/).
Joining Calm was my first executive role, where I was able to not only propose but also mandate strategy.

Like almost all startups, the engineering team was scattered when I joined.
Was our most important work creating more scalable infrastructure?
Was our greatest risk the failure to adopt leading programming languages?
How did we rescue the stuck [service decomposition initiative](https://craftingengstrategy.com/monolith-decomposition-strategy/)?

This strategy is where the engineering team and I aligned after numerous rounds of iteration,
debate, and inevitably some disagreement. As a strategy, it's both basic and also unambiguous
about what we valued, and I believe it's a reasonably good starting point for any [low scalability-complexity](https://lethain.com/quality/)
consumer product.

## Reading this document

To apply this strategy, start at the top with _Policy_. To understand the thinking behind this strategy, read sections in reverse order, starting with _Explore_, then _Diagnose_ and so on.
Relative to the default structure, this document has one tweak, folding the _Operation_ section in with _Policy_.

More detail on this structure in [Making a readable Engineering Strategy document](https://lethain.com/readable-engineering-strategy-documents).

## Policy & Operation

Our new policies, and the mechanisms to operate them are:

* **We are a product engineering company.**
    Users write in every day to tell us that our product has changed their lives for the better.
    Our technical infrastructure doesn't get many user letters--and this is unlikely to change going forward
    as our infrastructure is relatively low-scale and low-complexity.
    Rather than attempting to change that, we want to devote the absolute maximum possible attention to product engineering.
* **We exclusively adopt new technologies to create valuable product capabilities.**
    We believe our technology stack as it exists today can solve the majority of our current and future product roadmaps.
    In the rare case where we adopt a new technology, we do so because a product capability is inherently impossible
    without adopting a new technology.
    
    We do not adopt new technologies for other reasons. For example, we would not adopt a new technology because
    someone is interested in learning about it. Nor would we adopt a technology because it is 30% _better suited_
    to a task.
* **We write all code in the monolith.**
    It has been ambiguous if new code (especially new application code) should be written in our JavaScript monolith,
    or if all new code _must_ be written in a new service outside of the monolith.
    This is no longer ambiguous: all new code must be written in the monolith.

    In the rare case that there is a functional requirement that makes writing in the monolith implausible,
    then you should request an exception as described below.
* **Exceptions are granted by the CTO, and must be in writing.**
    The above policies are deliberately restrictive. Sometimes they may be wrong, and we will
    make exceptions to them. However, each exception should be deliberate and grounded in concrete
    problems we are aligned both on solving and how we solve them.
    If we all scatter towards our preferred solution, then we'll create negative leverage for Calm
    rather than serving as the engine that advances our product.
    
    All exceptions must be written. If they are not written, then you should operate as if it has not been granted.
    Our goal is to avoid ambiguity around whether an exception has, or has not, been approved.
    If there's no written record that the CTO approved it, then it's not approved.

Proving the point about exceptions, there are two confirmed exceptions to the above strategy:

1. **We are incrementally migrating to TypeScript.**
    We have found that static typing can prevent a number of our user-facing bugs.
    TypeScript provides a clean, incremental migration path for our JavaScript codebase,
    and we aim to migrate the entirety over the next six months.

    Our Web engineering team is leading this migration.
2. **We are evaluating Postgres Aurora as our primary database.**
    Many of our recent production incidents are caused by index scans
    for tables with high write velocity such as tracking customer logins.
    We believe Aurora will perform better under these workloads.

    Our Infrastructure engineering team is leading this initiative.

## Diagnose

The current state of our engineering organization:

* **Our product is not limited by missing infrastructure capabilities.**
    Reviewing our roadmap, there's nothing that we are trying to build today
    or over the next year that is constrained by our technical infrastructure.
* **Our uptime, stability and latency are OK but not great.**
    We have semi-frequent stability and latency issues in our application,
    all of which are caused by one of two issues.
    First, deploying new code with a missing index because it performed well enough in a test environment.
    Second, writes to a small number of extremely large, skinny tables have become expensive in combination
    with scans over those tables' indexes.
* **Our infrastructure team is split between supporting monolith and service workflows.**
    One way to measure technical debt is to understand how much time the team is spending
    maintaining the current infrastructure. Today, that is meaningful but not overwhelming
    work for our team of three infrastructure engineers supporting 30 product engineers.

    However, we _are_ finding infrastructure engineers increasingly pulled into debugging
    incidents for components moved out of the central monolith into our service architecture.
    This is partially due to increased inherent complexity, but it's more due to exposing
    lack of monitoring and ambiguous accountability in services' production incidents.
* **Our product and executive stakeholders experience us as competing factions.**
    Engineering exists to build and operate software in the company.
    Part of that is being easy to work with. We should not necessarily support every ask from Product
    if we believe they are misaligned with Engineering's goals (e.g. maintaining security),
    but it should generally provide a consistent perspective across our team.

    Today, our stakeholders believe they will get radically different answers to basic
    questions of capabilities and approach depending on who they ask. If they try to
    get a group of engineers to agree on an approach, they often find we derail into
    debate about approach rather than articulating a clear point of view that allows
    the conversation to move forward.
* **We're spending an outsized amount of time debating technology adoptions and rewrites.**
    Most of our disagreements stem from adopting new technologies or rewriting existing
    components into new technology stacks. For example, can we extend this feature or
    do we have to migrate it to a service before extending it?
    Can we add this to our database or should we move it into a new Redis cache instead?
    Is JavaScript a sufficient programming language, or do we need to rewrite this functionality in Go?

    This is particularly relevant to next steps around the ongoing services migration,
    which has been in-flight for over a year, but is yet to move any core production code.
* **We are spending more time on infrastructure and platform work than product work.**
    This is the combination of all the above issues, from the stability issues we are
    encountering in our database design, to the lack of engineering alignment on execution.
    This places us at odds with stakeholders' expectations that we are predominantly focused
    on new product development.

## Explore

Calm is a mobile application that guides users to build and maintain either a meditation or sleep habit.
Recommendations and guidance across content are individual to the user, but the content is shared across
all customers and is amenable to caching on a content delivery network (CDN).
As long as the CDN is available, the mobile application can operate despite the inability to access servers
(e.g. the application remains usable from a user's perspective, even if the non-CDN production infrastructure
is unreachable).

In 2010, enabling a product of this complexity would have required significant bespoke infrastructure,
along with likely maintaining a physical presence in a series of datacenters to run your software.
In 2020, comparable applications are generally moving towards maintaining as little internal infrastructure as possible.
This perspective is summarized effectively in Intercom's [Run Less Software](https://www.intercom.com/blog/run-less-software/)
and Dan McKinley's [Choose Boring Technology](https://mcfunley.com/choose-boring-technology).

New companies founded in this space view essentially all infrastructure as a commodity bought off your cloud provider.
This even extends to areas of innovation, such as machine learning, where the training infrastructure is typically
run on an offering like AWS Bedrock, and the model infrastructure is provided by Anthropic or OpenAI.
````

## File: llm/30000_resource-eng-driven-projects.md
````markdown
# How to resource Engineering-driven projects at Calm? (2020)
url: https://craftingengstrategy.com/project-resourcing-strategy

One of the recurring challenges in any organization is how to split your attention
across long-term and short-term problems. Your software might be struggling to scale
with ramping user load while also knowing that you have a series of meaningful security vulnerabilities
that need to be closed sooner than later. How do you balance across them?

These sorts of balance questions occur at every level of an organization.
A particularly frequent format is the debate between Product and Engineering
about how much time goes towards developing new functionality versus improving
what's already been implemented.
In 2020, Calm was growing rapidly as we navigated the COVID-19 pandemic,
and the team was struggling to make improvements, as they felt saturated by incoming new requests.
This strategy for resourcing Engineering-driven projects was our attempt to
solve that problem.

## Reading this document

To apply this strategy, start at the top with _Policy_. To understand the thinking behind this strategy, read sections in reverse order, starting with _Explore_.

More detail on this structure in [Making a readable Engineering Strategy document](https://lethain.com/readable-engineering-strategy-documents).

## Policy & Operation

Our policies for resourcing Engineering-driven projects are:

* We will protect one Eng-driven project per product engineering team, per quarter.
    These projects should represent a maximum of 20% of the team's bandwidth.
    Each project must advance a measurable metric,
    and execution must be designed to show progress on that metric within 4 weeks.
* These projects must adhere to [Calm's existing Engineering strategies](https://craftingengstrategy.com/product-eng-strategy/).
* We resource these projects first in the team's planning, rather than last.
    However, only concrete projects are resourced.
    If there are no concrete proposals, then the team won't have time budgeted for Engineering-driven work.
* Team's engineering manager is responsible for deciding on the project,
    ensuring the project is valuable,
    and pushing back on attempts to defund the project.
* Project selection does not require CTO approval, but you should escalate to the CTO if there's friction
    or disagreement.
* CTO will review Engineering-driven projects each quarter
    to summarize their impact and provide feedback to teams' engineering managers
    on project selection and execution.
    They will also review teams that did _not_ perform a project to understand why not.

As we've communicated this strategy, we've frequently gotten conceptual alignment
that this sounds reasonable, coupled with uncertainty about what sort of projects
should actually be selected. At some level, this ambiguity is an acknowledgment
that we believe teams will identify the best opportunities bottoms-up.
However, we also wanted to give two concrete examples of projects we're greenlighting in the
first batch:

* *Code-free media release*: historically, we've needed to make a number of pull requests
    to add, organize, and release new pieces of media. This is high urgency work,
    but Engineering doesn't exercise much judgment while doing it, and
    manual steps often create errors. We aim to track and eliminate these pull requests,
    while also increasing the number of releases that can be facilitated without
    scaling the content release team.
* *Machine-learning content placement*: developing new pieces of media is often a multi-week or month
    process. After content is ready to release, there's generally a debate on where to place the content.
    This matters for the company, as this drives engagement with our users,
    but it matters even more to the content creator, who is generally evaluated in terms of their content's
    performance.

    This often leads to Product and Engineering getting caught up in debates about how to
    surface particular pieces of content. This project aims to improve user engagement
    by surfacing the best content for their interests, while also giving the Content team
    several explicit positions to highlight content without Product and Engineering involvement.

Although these projects are similar, it's not intended that _all_
Engineering-driven projects are of this variety.
Instead it's happenstance based on what the teams view as
their biggest opportunities today.

## Diagnosis

Our assessment of the current situation at Calm is:

* We are spending a high percentage of our time on urgent but low engineering value tasks.
    Most significantly, about one-third of our time is going into launching, debugging,
    and changing content that we release into our product.
    Engineering is involved due to implementation limitations, not because our involvement adds inherent value
    (We mostly just make releases slowly and inadvertently introduce bugs of our own.)
* We have a bunch of fairly clear ideas around improving the platform
    to empower the Content team to speed up releases, and to eliminate the Engineering involvement.
    However, we've struggled to find time to implement them, or to validate that these ideas will work.
* If we don't find a way to prioritize, and succeed at implementing, a project
    to reduce Engineering involvement in Content releases, we will struggle to support
    our goals to release more content and to develop more product functionality this year
* Our Infrastructure team has been able to plan and make these kinds of investments stick.
    However, when we attempt these projects within our Product Engineering teams,
    things don't go that well.
    We are good at getting them onto the initial roadmap, but then
    they get deprioritized due to pressure to complete other projects.
* Our Engineering team of 20 engineers is not very fungible, largely due to
    specialization across roles like iOS, Android, Backend, Frontend, Infrastructure, and QA.
    We would like to staff these kinds of projects onto the Infrastructure team,
    but in practice that team does not have the product development experience to implement
    this kind of project.
* We've discussed spinning up a Platform team, or moving product engineers onto Infrastructure,
    but that would either (1) break our goal to maintain joint pairs between Product Managers and Engineering Managers,
    or (2) be indistinguishable from prioritizing within the existing team because it would still have
    the same Product Manager and Engineering Manager pair.
* Company planning is organic, occurring in many discussions and limited structured process.
    If we make a decision to invest in one project, it's easy for that project to get
    deprioritized in a side discussion missing context on why the project is important.

    These reprioritization discussions happen both in executive forums and in
    team-specific forums. There's imperfect awareness across these two sorts of forums.

## Explore

Prioritization is a deep topic with a wide variety of [popular solutions](https://en.wikipedia.org/wiki/Requirement_prioritization).
For example, many software companies rely on "RICE" scoring, calculating priority as (Reach times Impact times Confidence) divided by Effort.
At the other extreme are complex methodologies like [Scaled Agile Framework](https://en.wikipedia.org/wiki/Scaled_agile_framework).

In addition to generalized planning solutions, many companies carve out special mechanisms
to solve for particular prioritization gaps.
Google historically offered [20% time](https://en.wikipedia.org/wiki/Side_project_time) to allow
individuals to work on experimental projects that didn't align directly with top-down priorities.
Stripe's Foundation Engineering organization developed the concept of Foundational Initiatives
to prioritize cross-pillar projects with long-term implications, 
which otherwise struggled to get prioritized within the team-led planning process.

All these methods have clear examples of succeeding, and equally clear examples of struggling.
Where these initiatives have succeeded, they had an engaged executive sponsoring the practice's rollout,
including triaging escalations when the rollout inconvenienced supporters of the prior method.
Where they lacked a sponsor, or were misaligned with the company's culture, these methods
have consistently failed despite the fact that they've previously succeeded elsewhere.
````

## File: llm/31000_pos-acquisition-strategy.md
````markdown
# How to integrate Stripe's acquisition of Index? (2018)

While discussions around acquisitions often focus on
[technical diligence](https://lethain.com/engineering-in-mergers-and-acquisition/) and
deciding whether to make the acquisition, the integration that follows
afterwards can be even more complex.
There are few irreversible trapdoor decisions in engineering,
but decisions made early in an integration tend to be surprisingly durable.

This engineering strategy explores Stripe's approach to integrating
[their 2018 acquisition of Index](https://www.pymnts.com/news/partnerships-acquisitions/2018/stripe-pos-software-startup-index-acquisition/).
While a business book would focus on the rationale for the acquisition itself,
here that rationale is merely part of the diagnosis that defines
the integration tradeoffs. The integration itself is the area of focus.

Like most acquisitions, the team responsible for the integration has
only learned about the project after the deal closed,
which means early efforts are
a scramble to apply [strategy testing](/strategy-testing/)
to distinguish between optimistic dates and technical realities.

## Reading this document

To apply this strategy, start at the top with _Policy & Operation_. To understand the thinking behind this strategy, read sections in reserve order, starting with _Explore_.

More detail on this structure in [Making a readable Engineering Strategy document](https://lethain.com/readable-engineering-strategy-documents).

## Policy & Operation

We're starting with little shared context between the acquired and acquiring engineering
teams, and have a six month timeline to launch a joint product.
So our starting policy is a mix of a commitment to joint refinement and several
provisional architectural policies:

1. **Meet at least weekly until the initial release is complete**:
    the involved leadership from Stripe and Index will hold a weekly sync meeting
    to refine our approach until we fulfill our initial release timeline.

    This meeting is jointly owned by Stripe's Head of Traffic Engineering and
    Index's Head of Engineering.
1. **Minimize changes to tokenization environment**: because point-of-sale devices directly work with
     customer payment details, the API that directly supports the point-of-sale device
    must live within our secured environment where payment details are stored.

    However, any other functionality _must not_ be added to our tokenization environment.
2. **All other functionality must exist in standard environments**: except for the minimum necessary
    functionality moving into the tokenization environment, everything else must be operated in
    our standard, non-tokenization environments.
    In particular, any software that requires frequent changes, or introduces complex external dependencies,
    should exist in the standard environments.
3. **Defer making a decision regarding the introduction of Java to a later date**: the introduction of Java is incompatible
    with our existing engineering strategy, but at this point we've also been unable to align stakeholders on
    how to address this decision. Further, we see attempting to address this issue as a distraction
    from our timely goal of launching a joint product within six months.

    We will take up this discussion after launching the initial release.
1. **Escalations come to paired leads**: given our limited shared context across teams,
    all escalations must come to both Stripe's Head of Traffic Engineering and
    Index's Head of Engineering.
2. **Security review of changes impacting tokenization environment**: we need to move quickly to launch
    the combined point-of-sale and payments product, but we _must not_ cut corners on
    security to launch faster. Security must be included and explicitly sign off
    on any integration decisions that involve our tokenization environment

## Diagnose

There are generally four categories of acquisitions: talent acquisitions to bring on a talented team,
business acquisitions to buy a company's revenue and product, technology acquisitions to add a differentiated
capability that would be challenging to develop internally, and time-to-market acquisitions where you
could develop the capability internally but can develop it meaningfully faster by acquiring a company.

While most acquisitions have a flavor of several of these dimensions, this acquisition
is primarily a time-to-market acquisition aimed to address these constraints:

* Several of our largest customers are pushing for us to provide a point-of-sale device integrated
    with our API-driven payments ecosystem. At least one has implied that we either provide this
    functionality on a committed timeline or they may churn to a competitor.
* We currently have no homegrown expertise in developing or integrating with hardware such
    as point-of-sale devices.
    Based on other zero-to-one efforts internally, we believe it would take about a year to
    hire the team, develop and launch a minimum-viable product for a point-of-sale device integrated into our platform.
* Where we've taken a horizontal approach to supporting web payments via an API,
    at least one of our competitors, Square, has taken a vertically integrated approach.
    While their API ecosystem is less developed than ours, they are a plausible destination
    for customers threatening to churn.    
* We believe that at least one of our enterprise customers will churn if our best commitment is
    launching a point-of-sale solution 12 months from now.
* We've decided to acquire a small point-of-sale startup, which we will use to commit
    to a six month timeframe for supporting an integrated point-of-sale device with
    our API ecosystem.
* We will need to rapidly integrate the acquired startup to meet this timeline.
    We only know a small number of details about what this will entail.
    We _do_ know that point-of-sale devices directly operate on payment details
    (e.g. the point-of-sale device knows the credit card details of the card it reads).
    
    Our compliance obligations restrict such activity to our "tokenization environment",
    a highly secured and isolated environment with direct access to payment details.
    This environment converts payment details into a unique token that other environments
    can utilize to operate against payment details without the compliance overhead of
    having direct access to the underlying payment details.
* Going into this technical integration, we have few details about the acquired company's
    technology stack. We do know that they are primarily a Java shop running on AWS, where
    we are primarily a Ruby (with some Go) shop running on AWS.

## Explore

Prior to this acquisition, we have done several small acquisitions.
None of those acquisitions had a meaningful product to integrate with ours,
so we don't have much of an internal playbook to anchor our approach in.

We do have limited experience in integrating technical acquisitions from
prior companies we've worked in, along with talking to peers at other
companies to mine their experience.
Synthesizing those experiences, the recurring patterns are:

1. Usually deal teams have made certain commitments,
    or the acquired team has understood certain commitments,
    that will be challenging to facilitate.
    This is doubly true when you are unaware of what those commitments might be.

    If folks seem to be behaving oddly, it might be one such misunderstanding,
    and it's worth engaging directly to debug the confusion.
2. There should be an executive sponsor for the acquisition,
    and the sponsor is typically the best person to ask about the company's intentions.
    If you can't find the executive sponsor, or they are not engaged,
    try to recruit a new executive sponsor rather than trying to make
    things work without one.
2. Close the culture gap quickly where there's little friction,
    and cautiously where there's little trust.

    We do need to bring the acquired company into our culture,
    but we have years to do that. The most successful stories of doing this
    leaned on a mix of moving folks into and out of the acquired team rather than
    applying force.
3. The long-term cost of supporting a new technology stack is
    high, and in conflict with our technology strategy of consolidating on
    as few programming languages as possible.

    This is not the place to be flexible, as each additional feature
    in the new stack will
    take you further from your desired outcome.
4. Finally, find a way to derisk key departures. Things can go wrong
    quickly. One of the easiest starting points is consolidating
    infrastructure immediately, even if the product or software takes
    longer.

Altogether, this was not the most reassuring exploration: it was a bit
abstract, and much of our research returned strongly-held, conflicting perspectives.
Perhaps acquisitions, like starting a new company, is one of those places
where there's simply no right way to do it well.
````

## File: llm/32000_api-deprecation-strategy.md
````markdown
# How should Stripe deprecate APIs? (~2016)
url: https://craftingengstrategy.com/api-deprecation-strategy

While Stripe is a widely admired company for things like its
creation of the [Sorbet typer project](https://craftingengstrategy.com/stripe-sorbet-strategy/), I personally
think that Stripe's most interesting strategy work is also among its most subtle:
its willingness to significantly prioritize API stability.

This strategy is almost invisible externally.
Internally, discussions around it were frequent and detailed, but mostly confined to dedicated API design conversations.
API stability isn't just a technical design quirk, it's a foundational decision in an API-driven business,
and I believe it is one of the unsung heroes of Stripe's business success.

## Reading this document

To apply this strategy, start at the top with _Policy_. To understand the thinking behind this strategy, read sections in reverse order, starting with _Explore_.

More detail on this structure in [Making a readable Engineering Strategy document](https://lethain.com/readable-engineering-strategy-documents).

## Policy & Operation

Our policies for managing API changes are:

* **Design for long API lifetime.**
    APIs are not inherently durable. Instead we have to design thoughtfully
    to ensure they can support change.
    When designing a new API, build a test application that doesn't use this API,
    then migrate to the new API.
    Consider how integrations might evolve as applications change. Perform these migrations yourself to understand potential friction with your API.
    Then think about the future changes that _we_ might want to implement on our end.
    How would those changes impact the API, and how would they impact the application you've developed.

    At this point, take your API to API Review for initial approval as described below.
    Following that approval, identify a handful of early adopter companies
    who can place additional pressure on your API design, and test with them
    before releasing the final, stable API.
* **All new and modified APIs must be approved by API Review.**
    API changes may not be enabled for customers prior to API Review approval.
    Change requests should be sent to `api-review` email group.
    For examples of prior art, review the `api-review` archive for prior requests
    and the feedback they received.

    All requests must include a written proposal.
    Most requests will be approved asynchronously by a member of API Review.
    Complex or controversial proposals will require live discussions to ensure API Review members
    have sufficient context before making a decision.
* **We never deprecate APIs without an unavoidable requirement to do so.**
    Even if it's technically expensive to maintain support, we incur that support cost.
    To be explicit, we define API deprecation as _any_ change that would require customers to
    modify an existing integration.

    If such a change were to be approved as an exception to this policy,
    it must first be approved by the API Review, followed by our CEO.
    One example where we granted an exception was the deprecation of TLS 1.2 support due to PCI compliance obligations.
* **When significant new functionality is required, we add a new API.**
    For example, we created [`/v1/subscriptions`](https://docs.stripe.com/api/subscriptions) to
    support those workflows
    rather than extending [`/v1/charges`](https://docs.stripe.com/api/charges) to add subscriptions support.

<div class="bg-light-gray br4 ph3 pv1">

With the benefit of hindsight, a good example of this policy in action was the introduction of the Payment Intents APIs to maintain
compliance with [Europe's Strong Customer Authentication](https://support.stripe.com/questions/payment-intents-api-requirement-for-strong-customer-authentication-%28sca%29-compliance)
requirements. Even in that case the `charge` API continued to work as it did previously,
albeit only for non-European Union payments.

</div>

* **We manage this policy's implied technical debt via an API translation layer.**
    We release changed APIs into versions, tracked in our [API version changelog](https://docs.stripe.com/changelog).
    However, we only maintain one implementation internally, which is the implementation of the latest
    version of the API.
    On top of that implementation, a series of version transformations are maintained,
    which allow us to support prior versions without maintaining them directly.
    While this approach doesn't _eliminate_ the overhead of supporting multiple API versions,
    it significantly reduces complexity by enabling us to maintain just a single, modern implementation internally.
    
    All API modifications _must_ also update the version transformation layers to allow the new
    version to coexist peacefully with prior versions.
* **In the future, SDKs may allow us to soften this policy.**
    While a significant number of our customers have direct integrations with our APIs,
    that number has dropped significantly over time.
    Instead, most new integrations are performed via one of our official API SDKs.

    We believe that in the future, it may be possible for us to make more backwards
    incompatible changes because we can absorb the complexity of migrations into
    the SDKs we provide. That is certainly _not_ the case yet today.

## Diagnosis

Our diagnosis of the impact on API changes and deprecation on our business is:

* If you are a small startup composed of mostly engineers, integrating a new payments API seems easy.
    However, for a small business without dedicated engineers—or a larger
    enterprise involving numerous stakeholders—handling external API changes can be particularly challenging.

    Even if this is only marginally true, [we've modeled the impact of minimizing API changes](https://craftingengstrategy.com/api-deprecation-model/)
    on long-term revenue growth, and it has a significant impact, unlocking our ability to benefit from
    other churn reduction work.
* While we believe API instability directly creates churn, we also believe that API stability
    directly retains customers by increasing the migration overhead even if they wanted to change providers.
    Without an API change forcing them to change their integration, we believe that hypergrowth customers
    are particularly unlikely to change payments API providers absent a concrete motivation like an
    API change or a payment plan change.
* We are aware of relatively few companies that provide long-term API stability in general,
    and particularly few for complex, dynamic areas like payments APIs.
    We can't assume that companies that make API changes are ill-informed.
    Rather it appears that they experience a meaningful technical debt tradeoff between the API provider and API consumers,
    and aren't willing to consistently absorb that technical debt internally.
* Future compliance or security requirements—along the lines of our upgrade from TLS 1.2 to TLS 1.3 for PCI—may necessitate API changes.
    There may also be new tradeoffs exposed as we enter new markets with their own compliance regimes.
    However, we have limited ability to predict these changes at this point.
````

## File: llm/32100_api-deprecation-model.md
````markdown
# Systems model of API deprecation
url: https://craftingengstrategy.com/api-deprecation-model

In [How should Stripe deprecate APIs?](https://craftingengstrategy.com/api-deprecation-strategy/), the diagnosis
depends on the claim that deprecating APIs is a significant cause of customer churn.
While there is internal data that can be used to correlate deprecation with churn,
it's also valuable to build a model to help us decide if we believe that
correlation and causation are aligned in this case.

In this chapter, we'll cover:

1. What we learn from modeling API deprecation's impact on user retention
2. Developing a system model using the [lethain/systems](https://github.com/lethain/systems) package on GitHub.
    That model [is available in the lethain/eng-strategy-models](https://github.com/lethain/eng-strategy-models/blob/main/APIDeprecationModel.ipynb)
    repository
3. Exercising that model to learn from it

Time to investigate whether it's reasonable to believe that API deprecation
is a major influence on user retention and churn.

## Learnings

In an initial model that has 10% baseline for customer churn per round,
reducing customers experiencing API deprecation from 50% to 10% per round only increases
the steady state of integrated customers by about 5%.

![The image is a line graph titled "Customer Integration & Churn Over Time." It depicts four different data series, each represented by a line, plotted against the x-axis (labeled "Rounds") and y-axis (labeled "Size of Stock"). 

1. **Initial Integrated Customers (Blue Line):**
   - Starts near zero, then rises sharply before gradually leveling off towards a size of about 900.

2. **Initial Deprecation Impacted Customers (Orange Line):**
   - Begins at zero, increases more moderately, and levels off around a size of 300.

3. **Less Deprecation Integrated Customers (Green Line):**
   - Also starts near zero, rises rapidly, and approaches a size of 1000 before leveling off.

4. **Less Deprecation Deprecation Impacted Customers (Red Line):**
   - Starts at zero, increases slightly, and flattens out at a size below 100.

The graph has a legend positioned at the bottom-right corner to denote each line's corresponding data series.](https://craftingengstrategy.com/static/blog/strategy/api-deprecation-model-2.png)

<p class="img-desc i tc f6">Impact of 10% and 50% API deprecation on integrated customers</p>

However, if we eliminate the baseline for customer churn entirely, then we see a massive
difference between a 10% and 50% rate of API deprecation.

![The image is a line graph titled "Customer Integration & Churn Over Time." It tracks the size of stock over 100 rounds for four different scenarios. The x-axis represents the rounds, while the y-axis shows the size of stock, ranging from 0 to 6000.

### Lines:
1. **Blue Line:** Represents "LowDeprecationNoBaseline IntegratedCustomers." This line curves sharply upward, reaching the highest value among the four, nearing 6000 by the end.
   
2. **Orange Line:** Represents "LowDeprecationNoBaseline DeprecationImpactedCustomers." This line remains the lowest, rising gradually and reaching a bit over 1000.
   
3. **Green Line:** Represents "NoBaselineChurn IntegratedCustomers." It rises steadily and levels off around 1500.
   
4. **Red Line:** Represents "NoBaselineChurn DeprecationImpactedCustomers." It maintains a consistent upward trend but remains below the green line, finishing slightly above 1000.

### General Observations:
- The blue line shows the greatest growth over time.
- The orange line has the least growth.
- The graph has a clear legend explaining each line's significance.
- The lines demonstrate various customer integration and impact scenarios over time.](https://craftingengstrategy.com/static/blog/strategy/api-deprecation-model-4.png)

<p class="img-desc i tc f6">Impact of rates of API deprecation with zero baseline churn</p>

The biggest takeaway from this model is that eliminating API-deprecation churn alone
won't significantly increase the number of integrated customers.
However, we also can't fully benefit from reducing baseline churn without simultaneously reducing API deprecations.
Meaningfully increasing the number of integrated customers requires lowering both sorts of churn in tandem.

## Sketch

We'll start by sketching the model's happiest path: potential customers flowing into
engaged customers and then becoming integrated customers. This represents a customer
who decides to integrate with Stripe's APIs, and successfully completes that integration
process.

![The image depicts a simple flowchart with three stages represented by rounded rectangles, connected by arrows pointing to the right. 

1. The first rectangle is labeled "potential customers."
2. An arrow connects this to the second rectangle, labeled "engaged customers."
3. Another arrow connects this to the third rectangle, labeled "integrated customers."

The flowchart visually illustrates a progression or transformation of customers from potential to engaged and finally to integrated.](https://craftingengstrategy.com/static/blog/strategy/api-deprecation-simple.png)

<p class="img-desc i tc f6">Happiest path for Stripe API integration</p>

Business would be good if that were the entire problem space.
Unfortunately, customers do occasionally churn.
This churn is represented in two ways:

1. `baseline churn` where integrated customers leave Stripe for any number of reasons,
    including things like dissolution of their company
2. `experience deprecation` followed by `deprecation-influenced churn`, which represent
    the scenario where a customer decides to leave after an API they use is deprecated

There is also a flow for `reintegration`, where a customer impacted by API deprecation
can choose to update their integration to comply with the API changes.

Pulling things together, the final sketch shows five stocks and six flows.

![This image is a flow diagram illustrating the process of customer engagement and churn. Here's a detailed description:

1. **Potential Customers**:
   - The starting point is "potential customers," shown in a rectangular box.
   - An arrow points to the next stage, indicating progression.

2. **Engaged Customers**:
   - The next stage is labeled "engaged customers," also in a rectangular box.
   - There is an arrow labeled "initial integration" leading to the next stage.

3. **Integrated Customers**:
   - The box labeled "integrated customers" follows.
   - Two pathways emerge from this stage:
     - One arrow labeled "baseline churn" leading to "churned customers."
     - Another path leading to "experience deprecation."

4. **Deprecation-Impacted Customers**:
   - A box labeled "deprecation-impacted customers" follows the "experience deprecation" arrow.
   - Two pathways:
     - One arrow labeled "reintegrated" looping back to "integrated customers."
     - Another arrow indicating "deprecation-influenced churn" leading to "churned customers."

5. **Churned Customers**:
   - The final stage is "churned customers," shown in a rectangular box.
   - Receives inputs from both "baseline churn" and "deprecation-influenced churn."

The diagram uses clear labeling and directional arrows to depict customer transitions and the impact of experience deprecation on](https://craftingengstrategy.com/static/blog/strategy/api-deprecation-full.png)

<p class="img-desc i tc f6">Final version of systems model for API deprecation</p>

You could imagine modeling additional dynamics, such as recovery of churned customers,
but it seems unlikely that would significantly influence our understanding of how API deprecation
impacts churn.

## Reason

In terms of acquiring customers, the most important flows
are customer acquisition and initial integration with the API.
Optimizing those flows will increase the number of existing integrations.

The flows driving churn are baseline churn, and
the combination of API deprecation and deprecation-influenced churn.
It's difficult to move baseline churn for a payments API, as many churning
customers leave due to company dissolution.  From a revenue-weighted perspective,
baseline churn is largely driven by non-technical factors, primarily pricing.
In either case, it's challenging to impact this flow without significantly lowering margin.

Engineering decisions, on the other hand, have a significant impact on both the number of API deprecations,
and on the ease of reintegration after a migration.
Because the same work to support reintegration also supports the initial integration experience,
that's a promising opportunity for investment.

## Model

You can find the [full implementation of this model on GitHub](https://github.com/lethain/eng-strategy-models/blob/main/APIDeprecationModel.ipynb)
if you want to see the full model rather than these emphasized snippets.

Now that we have identified the most interesting avenues for experimentation,
it's time to develop the model to evaluate which flows are most impactful.

Our initial model specification is:

    # User Acquisition Flow
    [PotentialCustomers] > EngagedCustomers @ 100
    # Initial Integration Flow
    EngagedCustomers > IntegratedCustomers @ Leak(0.5)
    # Baseline Churn Flow
    IntegratedCustomers > ChurnedCustomers @ Leak(0.1)
    # Experience Deprecation Flow
    IntegratedCustomers > DeprecationImpactedCustomers @ Leak(0.5)
    # Reintegrated Flow
    DeprecationImpactedCustomers > IntegratedCustomers @ Leak(0.9)
    # Deprecation-Influenced Churn
    DeprecationImpactedCustomers  > ChurnedCustomers @ Leak(0.1)

Whether these are _reasonable_ values depends largely on how we think about the
length of each round. If a round was a month, then assuming half of integrated customers
would experience an API deprecation would be quite extreme. If we assumed it was a year,
then it would still be high, but there are certainly some API providers that routinely deprecate
at that rate. (From my personal experience, I can say with confidence that Facebook's Ads API deprecated
at least one important field on a quarterly basis in the 2012-2014 period.)

Admittedly, for a payments API this would be a high rate, and is intended primarily as a
contrast with more reasonable values in the exercise section below.

## Exercise

Our goal with exercising this model is to understand how much API deprecation impacts customer churn.
We'll start by charting the initial baseline, then move to compare it with a variety of scenarios
until we build an intuition for how the lines move.

![The image is a line graph titled "Customer Integration & Churn Over Time." It displays data about two types of customers over a series of "Rounds" plotted on the x-axis, ranging from 0 to 100. The y-axis represents the "Size of Stock," ranging from 0 to 1000.

There are two lines in the graph:

1. **Blue Line**: Labeled as "Initial Integrated Customers," it starts at the origin and increases rapidly at first, then slows down, approaching a plateau around 1000 as the rounds increase.

2. **Orange Line**: Labeled as "Initial Deprecation Impacted Customers," it also begins near the origin, rising quickly but reaching a lower plateau around 400 as the rounds increase.

The legend is located at the bottom right of the graph. The graph shows the dynamics of customer integration and impact over time, with integrated customers reaching a higher stable size compared to deprecation-impacted customers.](https://craftingengstrategy.com/static/blog/strategy/api-deprecation-model-1.png)

<p class="img-desc i tc f6">Initial model stabilizing integrated customers around 1,000 customers</p>

The initial chart stabilizes in about forty rounds, maintaining about 1,000 integrated customers
and 400 customers dealing with deprecated APIs.
Now let's change the experience deprecation flow to impact significantly fewer
customers:

    # Initial setting with 50% experiencing deprecation per round
    IntegratedCustomers > DeprecationImpactedCustomers @ Leak(0.5)
    
    # Less deprecation, only 10% experiencing per round
    IntegratedCustomers > DeprecationImpactedCustomers @ Leak(0.1)

After those changes, we can compare the two scenarios.

![The image is a line graph titled "Customer Integration & Churn Over Time." It depicts how different categories of customer stocks change over multiple rounds. The x-axis represents "Rounds," ranging from 0 to 100, and the y-axis represents the "Size of Stock," ranging from 0 to 1000.

There are four lines on the graph, each representing a different category:

1. **Blue Line (Initial IntegratedCustomers):**
   - Starts at the origin and increases steadily, approaching a plateau around 800.

2. **Orange Line (Initial DeprecationImpactedCustomers):**
   - Begins at the origin, grows steadily, and levels off around 300.

3. **Green Line (LessDeprecation IntegratedCustomers):**
   - Starts at the origin, rises more quickly than the blue line, leveling off slightly below 1000.

4. **Red Line (LessDeprecation DeprecationImpactedCustomers):**
   - Begins at the origin, increases slightly, and stabilizes just above 100.

The graph includes a legend at the bottom right, corresponding to each line's color and category. The green line represents the largest stock size, while the red line represents the smallest.](https://craftingengstrategy.com/static/blog/strategy/api-deprecation-model-2.png)

<p class="img-desc i tc f6">Impact of 10% and 50% API deprecation on integrated customers</p>

Lowering the deprecation rate significantly reduces the number of companies dealing with deprecations
at any given time, but it has a relatively small impact on increasing the steady state for integrated customers.
This must mean that another flow is significantly impacting the size of the integrated customers stock.

Since there's only one other flow impacting that stock, baseline churn, that's the one to exercise next.
Let's set the baseline churn flow to zero to compare that with the initial model:

    # Initial Baseline Churn Flow
    IntegratedCustomers > ChurnedCustomers @ Leak(0.1)
    
    # Zeroed out Baseline Churn Flow
    IntegratedCustomers > ChurnedCustomers @ Leak(0.0)

These results make a compelling case that baseline churn is
dominating the impact of deprecation. With no baseline churn, the number of integrated customers
stabilizes at around 1,750, as opposed to around 1,000 for the initial model.

![The image is a line graph titled "Customer Integration & Churn Over Time." It displays four distinct lines, each representing a different dataset related to customer integration and churn, plotted over 100 rounds on the x-axis. The y-axis represents the "Size of Stock."

The lines are as follows:

1. **Blue Line:** "Initial IntegratedCustomers" – Begins low and rises steadily before leveling off.
2. **Orange Line:** "Initial DeprecationImpactedCustomers" – Starts even lower and shows a slow increase, remaining the smallest throughout.
3. **Green Line:** "NoBaselineChurn IntegratedCustomers" – Exhibits a steep rise initially and becomes the highest by the end.
4. **Red Line:** "NoBaselineChurn DeprecationImpactedCustomers" – Shows a steady increase, starting below the blue line but finishing slightly above it.

The legend is in the lower right corner, identifying each line by color and description. Overall, the graph illustrates different trends and impacts of customer integration and churn over time.](https://craftingengstrategy.com/static/blog/strategy/api-deprecation-model-3.png)

<p class="img-desc i tc f6">Impact of eliminating baseline churn from model</p>

Next, let's compare two scenarios without baseline churn, where one has high API deprecation (50%)
and the other has low API deprecation (10%).

![The image is a line graph titled "Customer Integration & Churn Over Time." It illustrates how the size of stock changes over 100 rounds for different scenarios.

- **X-axis:** Represents the number of rounds, ranging from 0 to 100.
- **Y-axis:** Represents the size of the stock, ranging from 0 to 6000.

The graph includes four lines, each representing a different scenario:

1. **Blue Line** - "LowDeprecationNoBaseline IntegratedCustomers":
   - Steep rising curve.
   - Reaches the highest size of stock, about 5700 by round 100.

2. **Orange Line** - "LowDeprecationNoBaseline DeprecationImpactedCustomers":
   - Gradual rising curve.
   - Reaches a size of stock slightly above 1000 by round 100.

3. **Green Line** - "NoBaselineChurn IntegratedCustomers":
   - Moderate rising curve.
   - Reaches a size of stock around 1700 by round 100.

4. **Red Line** - "NoBaselineChurn DeprecationImpactedCustomers":
   - Slightly steeper than the orange line.
   - Reaches a size of stock around 1300 by round 100.

The legend is placed at the top center of the graph, identifying each line with its corresponding scenario.](https://craftingengstrategy.com/static/blog/strategy/api-deprecation-model-4.png)

<p class="img-desc i tc f6">Impact of rates of API deprecation with zero baseline churn</p>

In the case of two scenarios without baseline churn, we can see having an API deprecation rate of
10% leads to about 6,000 integrated customers, as opposed to 1,750 for a 50% rate of API deprecation.
More importantly, in the 10% scenario, the integrated customers line shows no sign of flattening, and
continues to grow over time rather than stabilizing.

The takeaway here is that significantly reducing either baseline churn or API deprecation magnifies the benefits of reducing the other.
These results also reinforce the value of treating churn reduction as a system-level optimization,
not merely a collection of discrete improvements.
````

## File: llm/33000_strategy-decompose-monolith.md
````markdown
# Should we decompose our monolith?

From their [first introduction in 2005](https://en.wikipedia.org/wiki/Microservices), the debate between adopting
a microservices architecture, a monolithic service architecture, or a hybrid between the two has become one of the
least-reversible decisions that most engineering organizations make.
Even migrating to a different database technology is _generally_ a less expensive change than moving from monolith
to microservices or from microservices to monolith.

The industry has in many ways gone full circle on that debate, from most hyperscalers in the 2010s partaking in
a multi-year monolith to microservices migration, to
[Kelsey Hightower's iconic tweet on the perils of distributed monoliths](https://x.com/kelseyhightower/status/940259898331238402):

> 2020 prediction: Monolithic applications will be back in style after people discover the drawbacks of distributed monolithic applications.
> \- @KelseyHightower

Even as popular sentiment has generally turned away from microservices, many engineering organizations have a bit of both,
often the remnants of one or more earlier but incomplete migration efforts. This strategy looks at a theoretical
organization stuck with a bit of both approaches, let's call it Theoretical Compliance Company,  which is looking to determine its path forward.

Here is Theoretical Compliance Company's service architecture strategy.

---

*This is an exploratory, draft chapter for a book on engineering strategy that I'm brainstorming in [#eng-strategy-book](https://lethain.com/tags/eng-strategy-book/).*
*As such, some of the links go to other draft chapters, both published drafts and very early, unpublished drafts.*

## Reading this document

To apply this strategy, start at the top with _Policy_. To understand the thinking behind this strategy, read sections in reverse order, starting with _Explore_, then _Diagnose_ and so on.
Relative to the default structure, this document has been refactored in two ways
to improve readability:
first, _Operation_ has been folded into _Policy_;
second, _Refine_ has been embedded in _Diagnose_.

More detail on this structure in [Making a readable Engineering Strategy document](https://lethain.com/readable-engineering-strategy-documents).

## Policy

Our policy for service architecture is documented here.
All exceptions to this policy **must** escalate _to_ a local Staff-plus engineer for their
approval, and then escalate _with_ that Staff-plus engineer to the CTO.
If you have questions about the policies, ask in `#eng-strategy`.

Our policy is:

1. **Business units should always operate in their own code repository and monolith.**
    They should not provision many different services. They should rarely work in other business units monoliths.
    There are nuances in the details: make decisions that bring us closer to the preceding sentence being true.
2. **New integrations across business unit monoliths should be done using gRPC.**
    The emphasis here is on _new_ integrations;
    it's desirable but not urgent to migrate existing integrations that use other implementations (HTTP/JSON, etc).

    When the decision is subtle (e.g. changes to an existing endpoint), optimize for
    business velocity rather than technical purity. When the decision is far from subtle (e.g. brand new endpoint),
    comply with the policy.
3. **Except for new business unit monoliths, we don't allow new services.**
    You should work within the most appropriate business unit monolith or within the existing infrastructure repositories.
    Provisioning a new service, unless it corresponds with a new business unit, always
    requires approval from the CTO in `#eng-strategy`.

    That approval generally will *not* be granted, unless
    the new service requires significantly different non-functional requirements than an existing monolith.
    For example, if it requires significantly higher compliance review prior to changes such as our existing
    payments service, or if it requires radically higher requests per second, and so on.
4. **Merge existing services into business-unit monoliths where you can.**
    We believe that each choice to move existing services back into a monolith should
    be made "in the details" rather than from a top-down strategy perspective. Consequently,
    we generally encourage teams to wind down their existing services outside of their business unit's monolith,
    but defer to teams to make the right decision for their local context.

## Diagnose

Theoretical Compliance Company has a complex history with decomposing our monolith.
We are also increasing our number of business units, while limiting our investment into
our core business unit. These are complex times, with a lot of constraints to juggle.
To improve readability, we've split the diagnosis into
two sections: "business constraints" and "engineering constraints."

Our business constraints are:

1. We sell business-to-business compliance solutions to other companies on an annual subscription.
    There is one major, established business line, and two smaller partially validated business lines
    that are intended to attach to the established business line to increase average contract value.
2. There are 2,000 people at the company. About 500 of those are in the engineering organization
    Within that 500, about 150 work on the broadest definition of "infrastructure engineering,"
    things like developer tools, compute and orchestration, networking, security engineering, and so on.
3. The business is profitable, but revenue growth has been 10-20% YoY, creating persistent pressure on spend
    from our board, based on mild underperformance relative to public market comparables.
    **Unless we can increase YoY growth by 5-10%, they expect us to improve free cash flow by 5-10% each year**,
    which jeopardizes our ability to maintain long-term infrastructure investments.
4. **Growth in the primary business line is shrinking.**
    The company's strategy includes spinning up more adjacent business units to increase average contract value with new products.
    **We need to fund these business units without increasing our overall budget**,
    which means budget for the new business units must be pulled away from either our core business or our platform teams.
    
    In addition to needing to fund our new business units, **there's ongoing pressure to make our core business more efficient**,
    which means either accelerating growth or reducing investment. It's challenging to accelerate growth while reducing investment,
    which suggests that most improvement will come from reducing our investment
5. Our methodology to allocate platform costs against business units does so proportionately to
    the revenue created by each business unit. **Our core business generates the majority of our revenue, which means it is accountable for the majority of our platform costs**,
    even if those costs are motivated by new business lines.
    
    This means that, even as the burden placed on platform teams increases due to spinning up multiple business units,
    there's significant financial pressure to reduce our platform spend because it's primarily represented as a cost to the core business
    whose efficiency we have to improve.
    This means we have little tolerance for anything that increases infrastructure overhead.

Our engineering constraints are:

1. Our infrastructure engineering team is 150 engineers supporting 350 product engineers,
    and it's certain that **infrastructure will not grow significantly in the foreseeable future**.
2. We spun up two new business units in the past six months, and **plan to spin up an additional two new business units**
    in the next year. Each business unit is led by a general manager, with engineering and product within that business unit
    principally accountable to that general manager. Our CTO and CPO still set practice standards, but it's situationally-specific
    whether these practice standards or direction from general manager is the last word on any given debate.

    For example, one business unit has been unwilling to support an on-call rotation for their product, because their general
    manager insists it is a wasteful practice. Consequently, that team often doesn't respond to pages, even when their service
    is responsible for impacting the stability of shared functionality.
3. We've modeled [how services and monoliths create overhead for both product and infrastructure organizations over time](https://lethain.com/services-overhead-model/),
    and have conviction that, in general, **it's more overhead for infrastructure to support more services**.
    We also found that in our organization, the rate of service ownership changing due to team reorganizations counteracts much of the initial productivity
    gains from leaving the monolith.
4. There is some tension between the two preceding observations: it's generally more overhead to have more services,
    but it's _even more_ overhead to have irresponsible business units breaking a shared monolithic service.
    For example, we can much more easily rate limit usage from a misbehaving service than fix a misbehaving codepath
    within a shared service.
5. We also have a payments service that moves money from customers to us.
    **Our compliance and security requirements for changes to this service are significantly higher**
    than for the majority of our software, because the blast radius is essentially infinite.
6. Our primary programming language is Ruby, which generally relies on blocking IO,
    and service-oriented architectures generally spend more time on blocking IO than monoliths.
    Similarly, Ruby is _relatively_ inefficient at serializing and deserializing JSON payloads,
    which our service architecture requires as part of cross-service communication.
7. We've previously attempted to decompose, and have **a number of lingering partial migrations that don't align cleanly with our current business unit ownership structure**.
    The number of these new services continues to grow over time,
    creating more burden on both infrastructure today and product teams in the future as they try to 
    maintain these services through various team reorganizations.

## Explore

In the late 2010s, most large or scaling companies adopted services to some extent.
Few adopted microservices, with the majority of adopters opting for a [service-oriented architecture](https://aws.amazon.com/compare/the-difference-between-soa-microservices/) instead.
[Kelsey Hightower's iconic tweet on the perils of distributed monoliths](https://x.com/kelseyhightower/status/940259898331238402) in 2020
captured the beginning of a reversal, with more companies recognizing the burden of operating service-oriented architectures.

In addition to the wider recognition of those burdens, many of the cloud infrastructure challenges that originally motivated service architectures began
to mellow. Most infrastructure engineers today _only_ know how to operate with cloud-native patterns, rather than starting from machine oriented approaches.
Standard database technologies like PostgreSQL have significantly improved capabilities. Cloud providers have fast local caches for quickly retrieving verified upstream packages.
Supply and cost of cloud compute is affordable. Slow programming languages are faster than they were a decade ago. Untyped languages have reasonable incremental paths
to typed codebases.

As a result of this shift, if you look at a new, emerging company,  it's particularly likely to have a monolith in one backend and one frontend programming language.
However, if you look at a five-plus-year-old company, you might find almost anything. One particularly common case is a monolith with most functionality,
and an inconsistent constellation of team-scoped macroservices scattered across the organization.

The shift away from [zero interest-rate policy](https://en.wikipedia.org/wiki/Zero_interest-rate_policy) has also impacted trends,
as service-oriented architectures tend to require more infrastructure to operate efficiently, such as service meshes, service provisioning and deprovisioning, etc.
Properly tuned, service-oriented architectures ought to be cost competitive, and potentially superior in complex workloads, but it's
hard to maintain the required investment in infrastructure teams when in a cost-cutting environment.
This has encouraged new companies to restrict themselves to monolithic approaches, and pushed existing companies to
_attempt_ to reverse their efforts to decompose their prior monoliths, with mixed results.
````

## File: llm/33000_stripe-sorbet.md
````markdown
# Why did Stripe build Sorbet? (~2017)
url: https://craftingengstrategy.com/stripe-sorbet-strategy

Many hypergrowth companies of the 2010s battled increasing complexity in
their codebase by [decomposing their monoliths](https://craftingengstrategy.com/monolith-decomposition-strategy/).
Stripe was somewhat of an exception, largely delaying decomposition until
it had grown beyond three thousand engineers and had accumulated a decade of development in its core Ruby monolith.
Even now, significant portions of their product are
maintained in the monolithic repository, and it's safe to say this was only possible
because of Sorbet's impact.

Sorbet is a custom static type checker for Ruby that was initially designed and implemented by Stripe engineers
on their Product Infrastructure team.
Stripe's Product Infrastructure had similar goals to other companies' Developer Experience or Developer Productivity teams,
but it focused on improving productivity through changes in the internal architecture of the codebase itself,
rather than relying solely on external tooling or processes.

This strategy explains why Stripe chose to delay decomposition for so long,
and how the Product Infrastructure team invested in developer productivity to deal with the challenges
of a large Ruby codebase managed by a large software engineering team with low average tenure caused by rapid hiring.

Before wrapping this introduction, I want to explicitly acknowledge that this
strategy was spearheaded by Stripe's Product Infrastructure team, not by me.
Although I ultimately became responsible for that team,
I can't take credit for this strategy's thinking.
Rather, I was initially skeptical, preferring an incremental migration to an existing
strongly-typed programming language, either Java for library coverage or Golang
for Stripe's existing familiarity.
Despite my initial doubts, the Sorbet project eventually won me over with its indisputable results.

## Reading this document

To apply this strategy, start at the top with _Policy_. To understand the thinking behind this strategy, read sections in reverse order, starting with _Explore_.

More detail on this structure in [Making a readable Engineering Strategy document](https://lethain.com/readable-engineering-strategy-documents).

## Policy & Operation

The Product Infrastructure team is investing in Stripe's
developer experience by:

* Every six months, Product Infrastructure will select its three highest priority areas to focus,
    and invest a significant majority of its energy into those.
    We will provide minimal support for other areas.

    We commit to refreshing our priorities every half after running the developer productivity survey.
    We will further share our results, and priorities, in each Quarterly Business Review.
* Our three highest priority areas for this half are:
    1. Add static typing to the highest value portions of our Ruby codebase,
        such that we can run the type checker locally and on the test machines to identify
        errors more quickly.
    2. Support selective test execution such that engineers can quickly determine and run
        the most appropriate tests on their machine rather than delaying until tests run
        on the build server.
    3. Instrument test failures such that we have better data to prioritize
        future efforts.
* Static typing is not a typical solution to developer productivity, so it
    requires some explanation when we say this is our highest priority area
    for investment. Doubly so when we acknowledge that it will take us 12-24 months
    of much of the team's time to get our type checker to an effective place.

    Our type checker, which we plan to name Sorbet, will allow us to continue developing
    within our existing Ruby codebase. It will further allow our product engineers
    to remain focused on developing new functionality rather than migrating existing
    functionality to new services or programming languages.
    Instead, our Product Infrastructure team will centrally absorb both the development
    of the type checker and the initial rollout to our codebase.
    
    It's possible for Product Infrastructure to take on both, despite its fixed size.
    We'll rely on a hybrid approach of deep-dives to add typing to particularly complex areas,
    and scripts to rewrite our code's Abstract Syntax Trees (AST) for less complex portions.
    In the relatively unlikely event that this approach fails, the cost to Stripe is of a small, known size:
    approximately six months of half the Product Infrastructure team, which is what we anticipate
    requiring to determine if this approach is viable.

    Based on our knowledge of Facebook's [Hack](https://hacklang.org/)
    project, we believe we can build a static type checker
    that runs locally and significantly faster than our test suite.
    It's hard to make a precise guess now, but we think less than 30 seconds to type our entire codebase,
    despite it being quite large.
    This will allow for a highly productive local development experience, even if we are not able to
    speed up local testing. Even if we do speed up local testing, typing would help us eliminate
    one of the categories of errors that testing has been unable to eliminate, which is passing
    of unexpected types across code paths which have been tested for expected scenarios but not
    for entirely unexpected scenarios.
    
    Once the type checker has been validated, we can incrementally prioritize adding typing
    to the highest value places across the codebase. We do not need to wholly type
    our codebase before we can start getting meaningful value.
* In support of these static typing efforts, we will advocate for product engineers at Stripe to begin development
    using the [Command Query Responsibility Segregation](https://en.wikipedia.org/wiki/Command_Query_Responsibility_Segregation)
    (CQRS) design pattern, which we believe
    will provide high-leverage interfaces for incrementally introducing static typing into our codebase.
* Selective test execution will allow developers to quickly run appropriate tests locally.
    This will allow engineers to stay in a tight local development loop, speeding up development
    of high quality code.

    Given that our codebase is not currently statically typed, inferring which tests to run is rather challenging.
    With our very high test coverage, and the fact that all tests will still be run before deployment to the
    production environment,
    we believe that we can rely on statistically inferring which tests are likely to fail when a given file is modified.
* Instrumenting test failures is our third, and lowest priority, project for this half.
    Our focus this half is purely on annotating errors for which we have high conviction about their source, whether infrastructure or test issues.
* For escalations and issues, reach out in the #product-infra channel.

## Diagnose

In 2017, Stripe is a company of about 1,000 people, including 400 software engineers.
We aim to grow our organization by about 70% year-over-year to meet increasing demand
for a broader product portfolio and to scale our existing products and infrastructure to accommodate user growth.
As our production stability has improved over the past several years, we have now turned
our focus towards improving developer productivity.

Our current diagnosis of our developer productivity is:

* We primarily fund developer productivity for our Ruby-authoring software engineers  via our Product Infrastructure team.
    The Ruby-focused portion of that team has about ten engineers on it today, and is unlikely to significantly grow in the future.
    (If we do expand, we are likely to staff non-Ruby ecosystems like Scala or Golang.)
* We have two primary mechanisms for understanding our engineer's developer experience.
    The first is standard productivity metrics around deploy time, deploy stability, test coverage, test time, test flakiness, and so on.
    The second is a twice annual developer productivity survey.
* Looking at our productivity metrics, our test coverage remains extremely high, with coverage above 99% of lines,
    and tests are quite slow to run locally. They run quickly in our infrastructure because they are multiplexed
    across a large fleet of test runners.
* Tests have become slow enough to run locally that an increasing number of developers
    run an overly narrow subset of tests, or entirely skip running tests until after pushing their changes.
    They instead rely on our test servers to run against their pull request's branch,
    which works well enough, but significantly slows down developer iteration time because the
    merge, build, and test cycle takes twenty to thirty minutes to complete.

    By the time their build-test cycle completes, they've lost their focus and maybe take several hours
    to return to addressing the results.
* There is significant disagreement about whether tests are becoming flakier due to test infrastructure
    issues, or due to quality issues of the tests themselves. At this point, there is no trustworthy dataset
    that allows us to attribute between those two causes.
* Feedback from the twice annual developer productivity survey supports the above diagnosis,
    and adds some additional nuance.
    Most concerning, although long-tenured Stripe engineers find themselves highly productive in our codebase,
    we increasingly hear in the survey that newly hired engineers with long tenures at other companies
    find themselves unproductive in our codebase.
    Specifically, they find it very difficult to determine how to safely make changes in our codebase.
* Our product codebase is entirely implemented in a single Ruby monolith.
    There is one narrow exception, a Golang service handling payment tokenization,
    which we consider out of scope for two reasons.
    First, it is kept intentionally narrow in order to absorb our SOC1 compliance obligations.
    Second, developers in that environment have not raised concerns about their productivity.

    Our data infrastructure is implemented in Scala. While these developers have concerns--primarily
    slow build times--they manage their build and deployment infrastructure independently, and the group remains relatively small.
* Ruby is not a highly performant programming language, but we've found it sufficiently efficient
    for our needs. Similarly, other languages are more cost-efficient from a compute resources perspective,
    but a significant majority of our spend is on real-time storage and batch computation.
    For these reasons alone, we would not consider replacing Ruby as our core programming language.
* Our Product Infrastructure team is about ten engineers, supporting about 250 product engineers.
    We anticipate this group growing modestly over time, but certainly sublinearly
    to the overall growth of product engineers.
* Developers working in Golang and Scala routinely ask for more centralized support,
    but it's challenging to prioritize those requests as we're forced to consider the return
    on improving the experience for 240 product engineers working in Ruby vs 10 in Golang
    or 40 data engineers in Scala.

    If we introduced more programming languages, this prioritization problem would become
    increasingly difficult, and we are already failing to support additional languages.
````

## File: llm/34000_pos-acquisition-strategy.md
````markdown
# How to integrate Stripe's acquisition of Index? (2018)
url: https://craftingengstrategy.com/index-acquisition-strategy

Discussions around acquisitions often focus on
[technical diligence](https://lethain.com/engineering-in-mergers-and-acquisition/) and
deciding whether to make the acquisition.
However, the integration that follows afterwards can be even more complex.
There are few irreversible trapdoor decisions in engineering,
but decisions made early in an integration tend to be surprisingly durable.

This engineering strategy explores Stripe's approach to integrating
[their 2018 acquisition of Index](https://www.pymnts.com/news/partnerships-acquisitions/2018/stripe-pos-software-startup-index-acquisition/).
While a business book would focus on the rationale for the acquisition itself,
here that rationale is merely part of the diagnosis that defines
the integration tradeoffs. The integration itself is the area of focus.

Like most acquisitions, the team responsible for the integration has
only learned about the project after the deal closed,
which means early efforts are
a scramble to apply [strategy testing](https://craftingengstrategy.com/strategy-testing/)
to distinguish between optimistic dates and technical realities.

## Reading this document

To apply this strategy, start at the top with _Policy & Operation_. To understand the thinking behind this strategy, read sections in reverse order, starting with _Explore_.

More detail on this structure in [Making a readable Engineering Strategy document](https://lethain.com/readable-engineering-strategy-documents).

## Policy & Operation

We're starting with little shared context between the acquired and acquiring engineering
teams, and have a six month timeline to launch a joint product.
So our starting policy is a mix of a commitment to joint refinement and several
provisional architectural policies:

1. **Meet at least weekly until the initial release is complete**:
    the involved leadership from Stripe and Index will hold a weekly sync meeting
    to refine our approach until we fulfill our initial release timeline.

    This meeting is jointly owned by Stripe's Head of Traffic Engineering and
    Index's Head of Engineering.
2. **Minimize changes to tokenization environment**: because point-of-sale devices directly work with
     customer payment details, the API that directly supports the point-of-sale device
    must live within our secured environment where payment details are stored.

    However, any other functionality _must not_ be added to our tokenization environment.
3. **All other functionality must exist in standard environments**: except for the minimum necessary
    functionality moving into the tokenization environment, everything else must be operated in
    our standard, non-tokenization environments.
    In particular, any software that requires frequent changes, or introduces complex external dependencies,
    should exist in the standard environments.
4. **Defer making a decision regarding the introduction of Java to a later date**: the introduction of Java is incompatible
    with our existing engineering strategy, but at this point we've also been unable to align stakeholders on
    how to address this decision. Further, we see attempting to address this issue as a distraction
    from our timely goal of launching a joint product within six months.

    We will take up this discussion after launching the initial release.
5. **Escalations come to paired leads**: given our limited shared context across teams,
    all escalations must come to both Stripe's Head of Traffic Engineering and
    Index's Head of Engineering.
6. **Security review of changes impacting tokenization environment**: we need to move quickly to launch
    the combined point-of-sale and payments product, but we _must not_ cut corners on
    security to launch faster. Security must be included and explicitly sign off
    on any integration decisions that involve our tokenization environment

## Diagnose

There are generally four categories of acquisitions: talent acquisitions to bring on a talented team,
business acquisitions to buy a company's revenue and product, technology acquisitions to add a differentiated
capability that would be challenging to develop internally, and time-to-market acquisitions where you
could develop the capability internally but can develop it meaningfully faster by acquiring a company.

While most acquisitions have a flavor of several of these dimensions, this acquisition
is primarily a time-to-market acquisition aimed at addressing these constraints:

* Several of our largest customers are pushing for us to provide a point-of-sale device integrated
    with our API-driven payments ecosystem. At least one has implied that we either provide this
    functionality on a committed timeline or they may churn to a competitor.
* We currently have no homegrown expertise in developing or integrating with hardware such
    as point-of-sale devices.
    Based on other zero-to-one efforts internally, we believe it would take about a year to
    hire the team, develop and launch a minimum-viable product for a point-of-sale device integrated into our platform.
* Where we've taken a horizontal approach to supporting web payments via an API,
    at least one of our competitors, Square, has taken a vertically integrated approach.
    While their API ecosystem is less developed than ours, they are a plausible destination
    for customers threatening to churn.    
* We believe that at least one of our enterprise customers will churn if our best commitment is
    launching a point-of-sale solution 12 months from now.
* We've decided to acquire a small point-of-sale startup, which we will use to commit
    to a six month timeframe for supporting an integrated point-of-sale device with
    our API ecosystem.
* We will need to rapidly integrate the acquired startup to meet this timeline.
    We only know a small number of details about what this will entail.
    We _do_ know that point-of-sale devices directly operate on payment details
    (e.g. the point-of-sale device knows the credit card details of the card it reads).
    
    Our compliance obligations restrict such activity to our "tokenization environment",
    a highly secured and isolated environment with direct access to payment details.
    This environment converts payment details into a unique token that other environments
    can utilize to operate against payment details without the compliance overhead of
    having direct access to the underlying payment details.
* Going into this technical integration, we have few details about the acquired company's
    technology stack. We do know that they are primarily a Java shop running on AWS, whereas
    we are primarily a Ruby (with some Go) shop running on AWS.

## Explore

Prior to this acquisition, we have done several small acquisitions.
None of those acquisitions had a meaningful product to integrate with ours,
so we don't have much of an internal playbook to anchor our approach in.

We do have limited experience in integrating technical acquisitions from
prior companies we've worked in, along with talking to peers at other
companies to mine their experience.
Synthesizing those experiences, some recurring patterns are:

1. Usually deal teams have made certain commitments,
    or the acquired team has understood certain commitments,
    that will be challenging to facilitate.
    This is doubly true when you are unaware of what those commitments might be.

    If folks seem to be behaving oddly, it might be one such misunderstanding,
    and it's worth engaging directly to debug the confusion.
2. There should be an executive sponsor for the acquisition,
    and the sponsor is typically the best person to ask about the company's intentions.
    If you can't find the executive sponsor, or they are not engaged,
    try to recruit a new executive sponsor rather than trying to make
    things work without one.
3. Close the culture gap quickly where there's little friction,
    and cautiously where there's little trust.

    We do need to bring the acquired company into our culture,
    but we have years to do that. The most successful stories of doing this
    leaned on a mix of moving folks into and out of the acquired team rather than
    applying force.
4. The long-term cost of supporting a new technology stack is
    high, and in conflict with our technology strategy of consolidating on
    as few programming languages as possible.

    This is not the place to be flexible, as each additional feature
    in the new stack will
    take you further from your desired outcome.
5. Finally, find a way to derisk key departures. Things can go wrong
    quickly. One of the easiest starting points is consolidating
    infrastructure immediately, even if the product or software takes
    longer.

Altogether, this was not the most reassuring exploration: it was a bit
abstract, and much of our research returned strongly-held, conflicting perspectives.
Perhaps acquisitions, like starting a new company, are among those places
where there's simply no right way to do it well.
````

## File: llm/34000_stripe-sorbet.md
````markdown
# Why did Stripe build Sorbet? (~2017).

**This is a work in progress draft.**

Hi

Finally, I think it's intellectually important to recognize the limits of my own involvement in the Sorbet strategy.
While I ultimately led the organization that built Sorbet at Stripe,
my organization did not include the Developer Productivity team when they decided to build Sorbet.
Indeed, I initially disagreed with the approach: I preferred investing in a migration to a strongly-typed language
(specifically Golang), rather than spending time on creating and maintaining a typing framework for Ruby.

Ultimately, while both approaches _might_ have worked, the Sorbet strategy _did_ work,
and it was probably the better choice because it allowed us to concentrate the investment
into a small team rather than spreading the cost across every team within Stripe.

## Reading this document

To apply this strategy, start at the top with _Policy_. To understand the thinking behind this strategy, read sections in reserve order, starting with _Explore_.

More detail on this structure in [Making a readable Engineering Strategy document](https://lethain.com/readable-engineering-strategy-documents).

## Policy & Operation

..

## Diagnose

* developer productivity surveys: Two stages – getting data, sitting with data ← imo this is how you learn; then picking a few specific projects and driving them; together this is the core DX team loop done on a one-off basis
    * imperfect: always something bad, so goal is sort of rotating what's bad
* migration of codebase will require many teams learning a new language
* adding ruby typing will allow a centralized team to make significant investments
* much of ruby typing can be done via the abstract syntax tree (AST)
* we can incrementally prioritize typing on highest value places
* ruby is not a high performance programing language, but it's generally good enough
    and we can get sufficient scale at a reasonable price
````

## File: llm/35000_good-vs-bad-strategy.md
````markdown
# Distinguishing good strategy from bad strategy

**This is a work-in-progress draft!**

One of the core challenges of evaluating strategy is that there's an apparent inevitability
to good strategy after the fact (of course it would work out), and an apparent cursedness
to bad strategy afterwards (of course it was a bad idea), which obscure whether the strategy
made sense in the moment it was created.

* believability is hard when history celebrates winners / senior leadership :-)




Discussion of distinguishing good versus bad strategy

---

*This is an exploratory, draft chapter for a book on engineering strategy that I'm brainstorming in [#eng-strategy-book](/tags/eng-strategy-book/).*
*As such, some of the links go to other draft chapters, both published drafts and very early, unpublished drafts.*


## Quick tools

* Is it obvious how to get paid twice by both complying with strategy and doing product work?




## Notes

* Quick refresher of Rumelt's discussion on bad strategy
* Take the ideas of https://lethain.com/solving-the-engineering-strategy-crisis/ wrt bad strategy
    and how to evaluate/determine.

* Sounds bad:
  * What decisions have been made differently as a result?
  * Do people reference it, or even remember it?
* Much worse:
  * Makes hard for people to do work
  * Makes it harder to accomplish the same output



* Even if your strategy isn't working well yet, just return to refinement phase. Many strategies don't work initially or "go out of alignment" over time and need to be adjusted
````

## File: llm/35000_is-this-strategy-good.md
````markdown
# Is this strategy any good?
url: https://craftingengstrategy.com/evaluating-strategy

We've read a lot of strategy at this point in the book.
We can judge a strategy's format, and its construction: both are useful things.
However, format is a predictor of quality, not quality itself.
The remaining question is, how should we assess whether a strategy is any good?

[Uber's service migration strategy](https://craftingengstrategy.com/uber-strategy/) unlocked
the entire organization to make rapid progress.
It also led to a sprawling architecture problem down the line.
Was it a great strategy or a terrible one? Folks can reasonably disagree,
but it's worthwhile developing our point of view on why we should prefer one
interpretation or the other.

This chapter will focus on:

* The various ways that are frequently suggested for evaluating strategies,
    such as input-only evaluation, output-only evaluation, and so on
* A rubric for evaluating strategies, and why a useful
    rubric has to recognize that strategies have to be evaluated
    in phases rather than as a unified construct
* Why ending a strategy is often a sign of a good strategist,
    and sometimes the natural reaction to a new phase in a strategy,
    rather than a judgment on prior phases
* How missing context is an unpierceable veil for evaluating other companies'
   strategies with high-conviction, and why you'll end up attempting to
   evaluate them anyway
* Why you can learn just as much from bad strategies as from good ones,
   even in circumstances where you are missing much of the underlying context

Time to refine our judgment about strategy quality a bit.

## How are strategies graded?

Before suggesting my own rubric, I want to explore how the industry appears to grade strategies in practice.
That's not because I particularly agree with them--I generally find each approach misses an important nuance--understanding
their flaws is a foundation to build on.

Grading strategy on its outputs is by far the most prevalent approach I've found in industry.
This is an appealing approach, because it does make sense that a strategy's results are more important
than anything else. However, this line of thinking can go awry.
We saw massive companies like Google move to service
architectures, and we copied them because if it worked for Google, it would likely work for us.
As discussed in the [monolith decomposition strategy](https://craftingengstrategy.com/monolith-decomposition-strategy/),
it did not work particularly well for most adopters.

The challenge with grading outputs is that it doesn't distinguish between
"alpha", how much better your results are because of your strategy, and "beta",
the expected outcome if you hadn't used the strategy.
For example, the [acquisition of Index](https://craftingengstrategy.com/index-acquisition-strategy/)
allowed Stripe to build a point-of-sale business line, but they were also on track to internally
build that business. Looking _only_ at outputs can't distinguish whether it would have been better
to build the business via acquisition or internally.
But one of those paths must have been the better strategy.

Similarly, there are also strategies that succeed, but do so at unreasonably high costs.
[Stripe's API deprecation strategy](https://craftingengstrategy.com/api-deprecation-strategy/) is a good example of a
strategy that was _extremely_ well worth the cost for the company's first decade,
but eventually became too expensive to maintain as the evolving regulatory environment created more overhead.
Fortunately, Stripe modified their strategy to allow some deprecations, but you can imagine an
alternate scenario where they attempted to maintain their original strategy, which would have
likely failed due to its accumulating costs.

Confronting these problems with judging on outputs, it's compelling to switch to the opposite lens and evaluate
strategy purely on its inputs. In that approach, as long as the sum of the strategy's parts make sense,
it's a good strategy, even if it didn't accomplish its goals.
This approach is very appealing, because it appears to focus _purely_ on the strategy's alpha.

Unfortunately I find this view similarly deficient.
For example, the [strategy for adopting LLMs](https://craftingengstrategy.com/llm-adoption-strategy/) offers a cautious approach to adopting LLMs.
If that company is outcompeted by competitors in the incorporation of LLMs, to the loss of significant revenue,
I would argue that strategy isn't a great one, even if it's rooted in a proper diagnosis and effective policies.
Doing good strategy requires reconciling the theoretical with the practical,
so we can't argue that inputs alone are enough to evaluate strategy work.
If a strategy is conceptually sound, but struggling to make an impact,
then its authors should continue to [refine it](https://craftingengstrategy.com/refine/).
If its authors take a single pass and ignore subsequent information that it's not working,
then it's a failed strategy, regardless of how thoughtful the first pass was.

While I find these mechanisms to be incomplete, they're still instructive.
By incorporating bits of each of these observations, we're surprisingly
close to a rubric that avoids each of these particular downfalls.

## Rubric for strategy

Balancing the strengths and flaws of the previous section's ideas,
the rubric I've found effective for evaluating strategy is:

1. **How quickly is the strategy refined?**
    If a strategy starts out bad, but improves quickly, that's a better strategy
    than a mostly right strategy that never evolves.
    Strategy thrives when its practitioners understand it is a living endeavor.
2. **How expensive is the strategy's refinement for implementing and impacted teams?**
    Just as culture eats strategy for breakfast,
    good policy loses to poor operational mechanisms every time.
    Especially early on, good strategy is validated cheaply.
    Expensive strategies are discarded before they can be validated,
    let alone improved.
3. **How well does the current iteration solve its diagnosis?**
    Ultimately, strategy does have to address the diagnosis it starts from.
    Even if you're learning quickly and at a low cost, at some point you
    do have to actually get to impact.
    Strategy must eventually be graded on its impact.
    

With this rubric in hand, we can finally assess the
[Uber's service migration strategy](https://craftingengstrategy.com/uber-strategy/).
It refined rapidly as we improved our tooling, minimized costs because
we had to rely on voluntary adoption, and solved its diagnosis extremely well.
So this was a great strategy, but how do we think about the fact that its diagnosis
missed out on the consequences of a wide-spread service architecture on developer productivity?

This brings me to the final component of the strategy quality rubric:
the recognition that strategy exists across multiple phases.
Each phase is defined by new information--whether or not this information is known
by the strategy's authors--that render the diagnosis incomplete.

The Uber strategy can be thought of as existing across two phases:

* Phase 1 used service provisioning to address developer productivity challenges
    in the monolith.
* Phase 2 was engaging with consequences of a sprawling service architecture.

All the good grades I gave the strategy are appropriate to the first phase.
However, the second phase was ushered in by the negative impacts to developer
productivity exposed by the initial rollout.
The second phase's grades on the rate of iteration, the cost, and the outcomes
were reasonable, but a bit lower than first phase.
In the subsequent years, the second phase was succeeded
by a third phase that aimed to address the second's challenges.

## Does stopping mean a strategy's bad?

Now that we have a rubric, we can use it to evaluate one of the
important questions of strategy: does giving up on a strategy mean
that the strategy is a bad one?

The vocabulary of strategy phases helps us here, and I think
it's uncontroversial to say that a new phase's evolution
of your prior diagnosis might make it appropriate to abandon a strategy.
For example, Digg owned our own servers in 2010, but
would certainly _not_ buy their own servers if they started
ten years later. Circumstances change.

Sometimes I also think that aborting a strategy in its
first phase is a good sign. That's generally true when
the rate of learning is outpaced by the cost of learning.
I recently sponsored a developer productivity strategy that
had some impact, but less than we'd intended.
We immortalized a few of the smaller pieces, and returned
further exploration to a [lower altitude strategy](https://craftingengstrategy.com/when-write-stratefy/)
owned by the teams rather than the high altitude strategy that I owned as an executive.

Essentially all strategies are competing with strategies at other altitudes,
so I think giving up on strategies, especially high altitude strategies,
is almost always a good idea.

## The unpierceable veil

Working within our industry, we are often called upon
to evaluate strategies from afar. As other companies rolled out
LLMs in their products or microservices for their architectures,
our companies pushed us on why we weren't making these changes as well.
The [exploration step](https://craftingengstrategy.com/explore/) of strategy helps determine
where a strategy might be useful for you, but even that doesn't really help
you evaluate whether the strategy or the strategists were effective.

There are simply too many dimensions of the rubric that you cannot evaluate
when you're far away. For example, how many phases occurred before the idea that
became the external representation of the strategy came into existence?
How much did those early stages cost to implement?
Is the _real_ mastery in the operational mechanisms that are never reported on?
Did the external representation of the strategy ever happen at all,
or is it the logical next phase that solves the reality of the internal
implementation?

With all that in mind, I find that it's generally impossible to accurately evaluate
strategies happening in other companies with much conviction.
Even if you want to, the missing context is an impenetrable veil.
That's not to say that you shouldn't try to evaluate their strategies,
that's something that you'll be forced to do in your own strategy work.
Instead, it's a reminder to keep a low confidence score in those appraisals:
you're guaranteed to be missing something.

## Learning despite quality issues

Although I believe it's quite valuable for us to judge the quality
of strategies, I want to caution against going a step further and
making the conclusion that you can't learn from poor strategies.
As long as you are aware of a strategy's quality, I believe you
can learn just as much from failed strategies as from great strategy.

Part of this is because often even failed strategies have early phases
that work extremely well. Another part is because strategies tend to
fail for interesting reasons. I learned just as much from Stripe's
failed rollout of agile, which struggled due to missing operational mechanisms, as I did from Calm's successful transition to focus primarily on product engineering.
Without a clear point of view on which of these worked,
you'd be at risk of learning the wrong lessons, but with forewarning you don't
run that risk.

Once you've determined a strategy was unsuccessful, I find it particularly valuable
to determine the strategy's phases and understand which phase and where in the [strategy steps](https://craftingengstrategy.com/strategy-steps/)
things went wrong. Was it a lack of operational mechanisms? Was the policy itself a poor match for
the diagnosis? Was the diagnosis willfully ignorant of a truculent executive?
Answering these questions will teach you more about strategy than only studying successful strategies,
because you'll develop an intuition for which parts truly matter.

## Summary

Finishing this chapter, you now have a structured rubric
for evaluating a strategy, moving beyond "good strategy" and "bad strategy" to
a nuanced assessment.
This assessment is not just useful for grading strategy, but makes it possible to
specifically improve your strategy work.

Maybe your approach is sound, but your operational mechanisms are too costly for
the rate of learning they facilitate.
Maybe you've treated strategy as a single iteration exercise, rather than
recognizing that even excellent strategy goes stale over time.
Keep those ideas in mind as we head into the final chapter
on [how you personally can get better at strategy work](https://craftingengstrategy.com/getting-better/).
````

## File: llm/37000_how-to-get-better-at-strategy.md
````markdown
# How to get better at strategy?
url: https://craftingengstrategy.com/getting-better

One of the most memorable quotes in Arthur Miller's _The Death of a Salesman_
comes from Uncle Ben, who describes his path to becoming wealthy as,
"When I was seventeen, I walked into the jungle, and when I was twenty-one I walked out. And by God I was rich."
I wish I could describe the path to learning engineering strategy in similar terms,
but by all accounts it's a much slower path. Two decades in, I am still learning
more from each project I work on.
This book has aimed to accelerate your learning path, but my experience is that there's
still a great deal left to learn, despite what this book has hoped to accomplish.

This final chapter is focused on the remaining advice I have to give on
how you can continue to improve at strategy long after reading this
book's final page.
Inescapably, this chapter has become advice on writing your own strategy
for improving at strategy.
You are already familiar with my general suggestions on creating strategy,
so this chapter provides focused advice on creating your own plan to get better at strategy.

It covers:

* Exploring strategy creation to find strategies you can learn from via public and private resources,
    and through creating learning communities
* How to diagnose the strategies you've found, to ensure you learn the right lessons from each one
* Policies that will help you find ways to perform and practice strategy
    within your organization, whether or not you have organizational authority
* Operational mechanisms to hold yourself accountable to developing a strategy practice
* My final benediction to you as a strategy practitioner who has finished reading this book

With that preamble, let's write this book's final strategy:
your personal strategy for developing your strategy practice.

## Exploring strategy creation

Ideally, we'd begin improving our engineering strategy skills by broadly reading publicly available examples.
Unfortunately, there simply aren't many easily available works to learn from others' experience.
Nonetheless, resources do exist, and we'll discuss the three categories
that I've found most useful:

1. Public resources on engineering strategy, such as companies' engineering blogs
2. Private and undocumented strategies available through your professional network
3. Learning communities that you build together, including ongoing learning circles

Each of these is explored in its own section below.

### Public resources

While there aren't as many public engineering strategy resources as I'd like,
I've found that there are still a reasonable number available.
This book collects a number of such resources in the appendix of [engineering strategy resources](https://craftingengstrategy.com/additional-resources/).
That appendix also includes some individuals' blog posts that are adjacent to this topic.
You can go a long way by searching and prompting your way into these resources.

As you read them, it's important to recognize that public strategies are often misleading,
as [discussed previously in evaluating strategies](https://lethain.com/distinguishing-good-vs-bad-strategy/).
Everyone writing in public has an agenda, and that agenda often means that they'll omit
important details to make themselves, or their company, come off well.
Make sure you read through the lines rather than taking things too literally.

### Private resources

Ironically, where public resources are hard to find, I've found it
much easier to find privately held strategy resources.
While private recollections are still prone to inaccuracies,
the incentives to massage the truth are less pronounced.

The most useful sources I've found are:

* *peers' stories* --
    strategies are often oral histories, and they are shared freely among
    peers within and across companies. As you build out your professional network,
    you can usually get access to any company's engineering strategy on any topic
    by just asking.
    
    There are brief exceptions. Even a close peer won't share a sensitive strategy before its
    existence becomes obvious externally, but they'll be glad to after it does.
    People tend to overestimate how much information companies can keep private anyway.
    Even reading recent job postings can usually expose a surprising amount about a company.
* *internal strategy archaeologists* --
    while surprisingly few companies formally collect their strategies into a repository,
    the stories are informally collected by the tenured members of the organization.
    These folks are the company's strategy archaeologists, and you can learn a great
    deal by explicitly consulting them
* *becoming a strategy archaeologist yourself* --
    whether or not you're a tenured member of your company, you can learn a tremendous amount by
    starting to build your own strategy repository.
    As you start collecting them, you'll interest others in contributing their strategies as well.
    
    As discussed in _Staff Engineer_'s section on the [Write five then synthesize](https://staffeng.com/guides/engineering-strategy/)
    approach to strategy,
    over time you can foster a culture of documentation where one didn't exist before.
    Even better, building that culture doesn't require any explicit authority, just an ongoing show of excitement.

There are other sources as well, ranging from attending the hallway track in conferences
to organizing dinners where stories are shared with a commitment to privacy.

### Working in community

My final suggestion for seeing how others work on strategy is to form
a [learning circle](https://lethain.com/rough-notes-learning-circles/).
I formed a [learning circle when I first moved into an executive role](https://lethain.com/crowdsourcing-cto-vpe-learning-circles/),
and at this point have been running it for more than five years.
What's surprised me the most is how much I've learned from it.

There are a few reasons why ongoing learning circles are exceptional for sharing strategy:

1. Bi-directional discussion allows so much more learning and understanding
    than mono-directional communication like conference talks or documents.
2. Groups allow you to learn from others' experiences and others' questions,
    rather than having to guide the entire learning yourself.
3. Continuity allows you to see the strategy at inception, during the rollout,
    and after it's been in practice for some time.
4. Trust is built slowly, and you only get the full details about a problem when
   you've already successfully held trust about smaller things.
   An ongoing group makes this sort of sharing feasible where a transient group does not.

Although putting one of these communities together requires a commitment,
they are the best mechanism I've found.
As a final secret, many people get stuck on how they can get invited to an existing
learning circle, but that's almost always the wrong question to be asking.
If you want to join a learning circle, make one. That's how I got invited to mine.

## Diagnosing your prior and current strategy work

Collecting strategies to learn from is a valuable part of improving,
but it's only the first step.
You also have to determine what to take away from each strategy.
For example, you have to determine whether Calm's approach to [resourcing Engineering-driven projects](https://craftingengstrategy.com/project-resourcing-strategy/)
is something to copy or something to avoid.

What I've found effective is to apply [the strategy rubric](https://craftingengstrategy.com/evaluating-strategy/) we developed in the "Is this strategy any good?" chapter
to each of the strategies you've collected.
Even by splitting a strategy into its various phases, you'll learn a lot.
Applying the rubric to each phase will teach you more.
Each time you do this to another strategy, you'll get a bit faster at applying
the rubric, and you'll start to see interesting, recurring patterns.

As you dig into a strategy that you've split into phases and applied the evaluation rubric to,
here are a handful of questions that I've found interesting to ask myself:

* How long did it take to determine a strategy's initial phase could be improved?
    How high was the cost to fund that initial phase's discovery?
* Why did the strategy reach its final stage and get repealed or replaced?
    How long did that take to get there?
* If you had to pick only one, did this strategy fail in its approach to
    exploration, diagnosis, policy or operations?
* To what extent did the strategy outlive the tenure of its primary author?
    Did it get repealed quickly after their departure, did it endure,
    or was it perhaps replaced during their tenure?
* Would you generally repeat this strategy, or would you strive to avoid repeating it?
    If you did repeat it, what conditions seem necessary to make it a success?
* How might you apply this strategy to your current opportunities and challenges?

It's not necessary to work through all of these questions for every strategy
you're learning from. I often try to pick the two that I think might be most
interesting for a given strategy.

## Policy for improving at strategy

At a high level, there are just a few key policies to consider for improving your strategic abilities.
The first is implementing strategy,
and the second is practicing implementing strategy.
While those are indeed the starting points,
there are a few more detailed options worth consideration:

* If your company has existing strategies that are not working, debug one and work to fix it.
    If you lack the authority to work at the company scope, then decrease altitude until
    you find an altitude you can work at. Perhaps setting Engineering organizational strategies
    is beyond your circumstances, but strategy for your team is entirely accessible.
* If your company has no documented strategies, document one to make it debuggable.
    Again, if operating at a high altitude isn't attainable for some reason, operate at a
    lower altitude that is within reach.
* If your company's or team's strategies are effective
    but have low adoption, see if you can iterate on operational mechanisms
    to increase adoption.
    Many such mechanisms require no authority at all, such as low-noise nudges
    or the [model-document-share](https://lethain.com/model-document-share/) approach.
* If existing strategies are effective and have high adoption,
    see if you can build excitement for a new strategy.
    Start by mining for which problems Staff-plus engineers and senior
    managers believe are important. Once you find one, you have a valuable
    strategy vein to start mining.
* If you don't feel comfortable sharing your work internally,
    then try writing proposals while only sharing them to a few trusted peers.

    You can even go further to only share proposals with trusted external peers,
    perhaps within a learning circle that you create or join.

Trying all of these at once would be overwhelming, so I recommend picking one
in any given phase.
If you aren't able to gain traction, then try another approach until something works.
It's particularly important to recognize in your diagnosis
where things are not working--perhaps you simply don't have the sponsorship you
need to enforce strategy so you need to switch towards suggesting strategies instead--and
you'll find something that works.

### What if you're not allowed to do strategy?

If you're looking to find one, you'll always unearth a reason
why it's not possible to do strategy in your current environment.

If you believe your current role prevents you from engaging in strategy work,
I've found two useful approaches:

1. *Lower your altitude* -- there's always a scale where you can perform strategy,
    even if it's just your team or even just yourself.

    Only you can forbid yourself from developing personal strategies.
2. *Practice rather than perform* -- organizations can only absorb so much strategy development
    at a given time, so sometimes they won't be open to you doing more strategy.
    In that case, you should focus on _practicing_ strategy work rather than directly
    performing it.

    Only you can stop yourself from practice.

Don't believe the hype: you can always do strategy work.

## Operating your strategy improvement policies

As the refrain goes, even the best policies don't accomplish much
if they aren't paired with operational mechanisms to ensure the policies
actually happen, and debug why they aren't happening.
It's tempting to overlook operations for personal habits, but that would be a mistake.
These habits profoundly impact us in the long term, yet they're easiest to neglect because others rarely inquire about them.

The mechanisms I'd recommend:

* Clearly track the strategies you've implemented, refined, documented, or read.
    Maintain these in a document, spreadsheet, or folder that makes it easy to monitor your progress.
* Review your tracked strategies every quarter: are you working on the expected number
    and in the expected way? If not, why not?

    Ideally, your review should be done in community with a peer or a learning circle.
    It's too easy to deceive yourself, it's much harder to trick someone else.
* If your periodic review ever discovers that you're simply not doing the work you expected,
    sit down for an hour with someone that you trust--ideally someone equally or more experienced than you--and
    debug what's going wrong. Commit to doing this _before_ your next periodic review.

Tracking your personal habits can feel a bit odd,
but it's something I highly recommend.
I've been setting and tracking personal goals for some time now—for example,
in my [2024 year in review](https://lethain.com/2024-in-review/)—and have benefited greatly from it.

### Too busy for strategy

Many companies convince themselves that they're too much in a rush to make good decisions.
I've certainly gotten stuck in this view at times myself,
although at this point in my career I find it increasingly difficult
to not recognize that I have a number of tools to create time for strategy,
and an obligation to do strategy rather than inflict poor decisions on
the organizations I work in. Here's my advice for creating time:

* If you're not tracking how often you're creating strategies, then start there.
* If you've not worked on a single strategy in the past six months, then start with one.
* If implementing a strategy has been prohibitively time consuming, then focus on practicing a strategy instead.

If you do try all those things and still aren't making progress,
then accept your reality: you don't view doing strategy as particularly important.
Spend some time thinking about why that is, and if you're comfortable with your answer,
then maybe this is a practice you should come back to later.

## Final words

At this point, you've read everything I have to offer on drafting engineering strategy.
I hope this has refined your view on what strategy can be in your organization,
and has given you the tools to draft a more thoughtful
future for your corner of the software engineering industry.

What I'd never ask is for you to wholly agree with my ideas here. They are my best thinking
on this topic, but strategy is a topic where I'm certain Hegel's world view is the correct one:
even the best ideas here are wrong in interesting ways, and will be surpassed by better ones.
````

## File: llm/40000_strategy-notes.md
````markdown
# Strategy resources
url: https://craftingengstrategy.com/additional-resources

One of the hardest parts of learning about engineering strategy
is finding useful resources on a topic where so much is kept
private. This appendix highlights some of the public resources
that I've found valuable during my learning experience.

## My prior writing

* [Writing an engineering strategy](https://lethain.com/eng-strategies/) is a chapter from
    *[The Engineering Executive's Primer](https://lethain.com/eng-execs-primer/)* on setting engineering strategy as an executive
* [Write five, then synthesize](https://lethain.com/good-engineering-strategy-is-boring/) is a chapter from
    *[Staff Engineer](https://staffeng.com/)* on driving engineering strategy without executive authority
    (primarily through documentation)

## Books

In addition to my own *[Staff Engineer](https://staffeng.com/)*
and *[The Engineering Executive's Primer](https://lethain.com/eng-execs-primer/)*,
both of which have chapters on engineering strategy, related books that I would encourage reading are:

* *[Architecture Modernization](https://www.manning.com/books/architecture-modernization)*
    by Nick Tune with Jean-Georges Perrin -- covers much of the same topics as *Technology Strategy Patterns*
    and *The Value Flywheel Effect*, but often with more recent examples and references given its later publication date
* *[Enterprise Architecture as Strategy](https://lethain.com/notes-on-enterprise-architecture-as-strategy/)*
    by Jeanne Ross, Peter Weill, and David Robertson --- an interesting read from 2006 on
    the evolution of software (e.g. IT in that era's vernacular) maturity within businesses,
    and deciding among strategies for coupling and integration across business units    
* *[Technology Strategy Patterns](https://lethain.com/notes-on-the-technology-strategy-patterns/)* by Eben Hewitt -- a method-focused book
    on creating and communicating engineering strategy
* *[The Phoenix Project](https://www.amazon.com/Phoenix-Project-DevOps-Helping-Business-ebook/dp/B078Y98RG8/)* by Kim, Behr, and Spafford -- a
    modern retelling of Goldratt's *[The Goal](https://www.amazon.com/Goal-Process-Ongoing-Improvement/dp/0884271951)*,
    which shows how to model and resolve problems using constraint optimization.
    Previously, I would not have considered this a strategy book, but as my opinion on what strategy is
    evolves (mapping plus guiding policies), I think it demonstrates a useful mapping strategy    
* *[The Value Flywheel Effect](https://lethain.com/notes-on-the-value-flywheel-effect)* by Anderson, McCann, and O'Reilly -- an introduction
    to Wardley maps via an exploration of Liberty Mutual's rationale for serverless
* *[Wardley Maps](https://medium.com/wardleymaps/on-being-lost-2ef5f05eb1ec)* by Simon Wardley explains
    how to use Wardley Maps to understand and improve strategy    

Additionally, I'd recommend these general books. They don't focus on engineering strategy,
but I've found them quite useful:

* *[Good Strategy, Bad Strategy](https://www.amazon.com/Good-Strategy-Bad-Difference-Matters-ebook/dp/B004J4WKEC/)* by
    Richard Rumelt -- the most helpful strategy book that I have ever read, because it actually provides a usable
    definition of strategy
* *[How Big Things Get Done](https://www.amazon.com/How-Big-Things-Get-Done-ebook/dp/B0B3HS4C98/) by Bent Flyvbjerg and Dan Gardner --  a
    fascinating look at why some [megaprojects](https://en.wikipedia.org/wiki/Megaproject) fail so resoundingly and why others succeed under budget and under schedule.
    Connects to many related topics, such as how [benchmarking](https://lethain.com/benchmarking/) can help evaluate guiding policies within a strategy    
* *[The Crux](https://lethain.com/notes-on-the-crux/)* by Richard Rumelt -- another good book by Richard Rumelt,
    this one more oriented on how to create strategies and why strategy creation often fails.
    (And less structurally focused on documenting strategies than *Good Strategy, Bad Strategy*.)
* *[Thinking in Systems: A Primer](https://www.amazon.com/Thinking-Systems-Donella-H-Meadows-ebook/dp/B005VSRFEA/)* by
    Donella Meadows -- a book on systems thinking, which for a long time was my sole tool for mapping things around me.
    This is not a software engineering book, but provides a lens into a useful mapping mechanism that you can apply to
    software and software development ([Why limiting work-in-progress works](https://lethain.com/limiting-wip/) is one example of
    me using systems thinking to model a software system)

## Case studies

Every discussion of engineering strategy includes a weary remark about how few strategies are
publicly documented. Acknowledging that concern, some case studies that I've found helpful:

* [Magnitudes of exploration](https://lethain.com/magnitudes-of-exploration/) documented a public version of Stripe's Engineering strategy
* *The Value Flywheel Effect* (linked under "Books" header above) is a good case study of Liberty Mutual's engineering strategy, and additionally includes case studies for A Cloud Guru, Workgrid, and BBC
* [Run less software](https://www.intercom.com/blog/run-less-software/) by Rich Archbold -- a fantastic writeup of
    a cornerstone of Intercom's engineering strategy
* [How Big Technical Changes Happen at Slack](https://slack.engineering/how-big-technical-changes-happen-at-slack/) by Adams and Rodgers -- this is not
    quite Slack's engineering strategy, but it has many components of their engineering strategy within it
* [The difficult teenage years: Setting tech strategy after a launch](https://medium.com/ft-product-technology/the-difficult-teenage-years-setting-tech-strategy-after-a-launch-7f42eb94a424) by Anna Shipman -- a look at
    FT's engineering strategy, particularly one that wasn't _really_ defined until somewhat late in the lifecycle
    (which is an extremely common occurrence, even if we don't admit it)

A few more resources that are either case study-ish or engineering-ish, so they don't
quite fit in the above list, but are nonetheless relevant reads:

* [BoringTechnology.club](https://boringtechnology.club/) by Dan McKinley -- a guiding principle that many engineering strategies include
* [GitLab Strategy](https://handbook.gitlab.com/handbook/company/strategy/) -- ok, it's actually the GitLab company strategy.
    but given they're a technology company that builds technology for technologists, it's an interesting read despite being
    at a slightly higher altitude than an engineering strategy

The internet is an unruly place, and I'm sure by the time that you're reading this,
many more excellent writeups will exist as well.
````
