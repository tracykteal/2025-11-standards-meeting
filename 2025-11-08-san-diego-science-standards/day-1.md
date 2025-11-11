---
title: Day 1
subtitle: Setting the Context, Building the Core, Designing the Movement
description: On the first day of the workshop we set context, introduced each other, ideated a preferable future, chose an organizing metaphor, and decided a way to move forward together in our second day.
---

# Setting Context

Before the in-person meeting, we went through the context of where the group is, and what we are all thinking and expecting to get out of the meeting. In this two-hour virtual call we tried to set some of the intention that our role in this workshop was to work "bottom-up" rather than "top-down"; we are aware of many of the incentive problems in the scholarly ecosystem, but in the group we are bringing together have limited direct ability to influence or change them — especially in two days. Our role, however, can be to enable new possibilities through technology, organizational connections, and sparks of new ideas that come from these in-person events. We can show, not tell, what exciting things are possible in scientific communication. As we shared in that meeting, especially our ambitious goals of introducing new formats for scientific communication someone inevitably shared that [xkcd comic](https://xkcd.com/927) about "there being 14 competing standards… now 15." It's funny because it's true — **_sometimes_**. We tried to identify some of the paradigm shifts at play — AI, cloud computing, distributed & composable research — and why sometimes those efforts need new ways to communicate.

> The medium of communication determines what you can communicate; and professional scientific communication is based on print.

**The way we do science has changed, but the way we communicate it has not kept up.** To illustrate through an example of standards evolution we introduced a case study on the format evolution of compressed and distributed scientific data; from ZIP --> HDF5 --> Zarr, and how the format changed to suit new capabilities and ultimately has enabled new ecosystems with each evolution. You can read the full case study here [@zip-to-zarr].

:::{figure #fig-zip-to-zarr} zip-to-zarr.png
We presented a case study of 30 years of evolution in sharing scientific data, from zip files in the 1989 to HDF5 that introduced structured metadata alongside binary arrays to open up parallel IO on clusters to Zarr introduced in 2015 that enabled distributed data-access in a simplified, cloud-native way. These new formats changed the ecosystem at each stage, and also brought with them the best practices from the standard before.
:::

We also shared a case study on Jupyter and JupyterHub, where Carol Willing talked about the beginnings of these conversations that started with a dream, ambition, values, and a community of extremely talented people. Both of these tools and standards a decade later have millions of users and support unique and **fundamentally** new use cases that were not previously possible.

> We invited participants to dream, to choose an open, community approach, and execute.

## Lightning Talks

To further set the stage, we invited lightning talks from Quarto, eLife, Creative Commons, arXiv, JATS, COAR Notify, Stencila, NueroLibre, openRxiv, Curvenote, OpenAlex, and MECA. These set a baseline understanding of some of these tools and approaches in play and the roles that people in the room are working on that can weave together and interoperate.

# Ideation and Group Discussion

We prompted the group to ideate, dream on an idealistic future, and then focus on concrete actions that we could take in the next day and a half that would make progress towards that future. We took 10 minutes and wrote ideas on sticky notes. Then we paired up to discuss, identify themes and create new ideas. Pairs then connected into groups of 5 or 6, and those groups reported out on the themes. 

> What do you wish was possible in scientific communication that is not possible or broadly adopted today?

:::{figure #fig-ideas} ideas.png
A small sample of some of the brainstorming and ideas from the group.
:::

## Common Themes

Across all groups, several recurring themes and also some concerns and opportunities around artificial intelligence surfaced:

Component-based and modular science
: Multiple groups emphasized breaking research into smaller, composable units—figures, datasets, methods—that could be recombined for different audiences (policy makers, educators, the public). These "component pieces" would form a new modular infrastructure for knowledge and could come with their own attribution and licensing. 

Computational content — built in, not bolted on
: Participants highlighted that computation should be natively included in the research narrative, not an afterthought. The goal is to treat code, data, and visualizations as first-class objects within the scientific record—interwoven with text and metadata, not hidden in supplements or external notebooks. Projects like Stencila, Curvenote, MyST, and Quarto were cited as leading examples of this integrated approach, where execution, interactivity, and reproducibility are embedded directly into the document itself.

Accessibility and education
: Many wanted to ensure research outputs can reach younger learners and non-experts, through interactive and modular content rather than static PDFs. Education was recognized as the historical vector of adoption for new scientific tools (e.g., Jupyter, R Markdown, Quarto, MyST).

Interoperability and standardization
: Participants stressed the need for shared schemas or "record locators" for research objects to make data, code, and media discoverable and reusable across distributed systems. This would remove the friction of incompatible formats between repositories and journals and make it possible to more easily link components together.

Human connection amid automation
: Despite technical focus, there was an emotional thread—preserving human relationships and trust networks in a landscape increasingly mediated by algorithms and AI filters. 

Trust, reputation, and accountability
: Participants worried about how to maintain human accountability in an era of AI-generated content and papermills. Identity and persistent identifiers for people (not just papers) were seen as one important component to rebuild trust and reputation in the scientific record. 

Attribution and licensing
: When modular components of science - data, code, images - can be more easily distributed or remixed, participants recognized that these components can then come with their own attribution and licensing, and we can build that into our technologies and approaches. 

Quality versus quantity in publishing
: The flood of low-quality or fraudulent content is overwhelming peer review and submission. Some groups discussed using AI-assisted review as "fighting fire with fire," with both potential and pitfalls.

In the group discussion, we came up with a metaphor [@cite] as an organizing principle to break into groups to get towards more concrete ideas to progress on these ideas in the next few days.

> What are the pathways to getting there that we can make progress on together **tomorrow**?

:::{figure #fig-breakout-1} breakout-1.png
Working together in small groups on various ideas.
:::

# The Bedrock–Soil–Flowers Metaphor 🌸🌷🌻

The group aligned on a three-layer ecological metaphor to describe the evolving structure of scientific knowledge:

## Bedrock – The Foundational Content

Represents the raw scientific materials: datasets, code, preprints, lab notes, and other primary research artifacts. It is the substrate upon which all higher layers depend—analogous to the geological foundation of an ecosystem. Participants described it as "boring but essential": the invisible, structured layer that ensures reliability, provenance, and persistence. Some proposed a "dynamic bedrock"—still foundational but continuously reshaped as new data, formats, and schemas emerge — this is especially true from an adoption perspective of existing tools in the room that want to use this format, but not be locked into something that isn't flexible.

:::{card} 🪨 Describing the Bedrock
:url: ./bedrock.md
We took notes on an architecture for the open exchange of scientific ideas that is accessible by developers and includes computational content and data as well as bakes in licensing and attribution in modular ways.
:::

## Soil – The Connecting Layer

The soil digests, organizes, and connects the bedrock materials—metadata, graphs of relationships, citation networks, peer review, and trust signals. It represents context, curation, and integration: where reputation systems, provenance graphs, and aggregation tools (like Scopus, CORE, or Google Scholar) operate. The soil also filters and moderates quality, providing "nutrients" that enrich the bedrock and allow meaningful reuse of content. Trust was seen as growing from the soil[^trust]:

> If we can trust the bedrock, we can trust the flowers—but the soil makes it possible for the flowers to grow

[^trust]: Others also commented that trust is likely in all layers of our metaphor, not just the "soil"!

## Flowers (the ecosystem) – The Visible, Dynamic Outputs and Applications

Flowers (and trees and shrubbery) represent applications, interfaces, and experiences built atop the lower layers. These are the journals, educational tools, visualizations, interactive notebooks, and AI-driven summaries. This is the layer that the public, educators, and policymakers engage with—the visible ecosystem that blooms from solid foundations and fertile connections

It encompasses both human-curated and AI-generated outputs—the "living ecosystem" of scientific communication. These applications often have the easiest time attracting new funding or excitement, but ultimately rely on the underlying layers to deliver value.

## Alignment and Insights

Trust propagates upward
: A trustworthy and transparent "bedrock" is made possible through identifying the connections between research objects, and ultimately new applications/experiences that can provide different curation, badging and labelling services that also contribute meaningful and reusable data.

Quality can tolerate imperfection
: The group agreed the bedrock can also contain low quality outputs; open, messy data/resources _are acceptable_ as long as filtering and curation (the soil/ecosystem) evolve accordingly and/or communities have the ability to self organize. This mirrors many of the existing cultures decoupling dissemination from review. 

Ecosystem thinking
: Each layer enables the next; no single actor can build all three. The system's resilience comes from modularity and interoperability.

Strategic focus
: Participants agreed to identify "boring but high-leverage" components—standards, schemas, and identifiers—that quietly enable everything else.

> The bedrock is the structured scientific content; the soil is the web of connections, curation, and trust; and the flowers are the dynamic, interactive ways science reaches people. We need all three layers for the ecosystem of knowledge to thrive.

# Break into groups to think through the How

## Bedrock

In this group the overall conversation centered around Scientific content produced in granular form so others can reuse, consume, and remix. The group decided to collaborate on a schema/architecture for the open exchange of scientific content, ensuring it is web-native, cloud ready, and enables new AI workflows. The scope of the effort for the workshop was to create a small library of schemas, examples, and tests. We identified existing tools and ideas in Stencila, MyST, Quarto, Curvenote, Pandoc, JATS, and schema.org that would be the basis for this new format. Starting with authoring tools enables the researcher to be directly involved in the production of something that is standards compliant. We also had advisors from Creative Commons, who helped identify places where licensing and attribution can be embedded directly in the workflows.

The general approach we sketched out for Day 2 was:

- Identify the units of scientific communication (figures, charts, paragraphs)
- Ensure that these include license and attribution at all levels
- Ensure any schema can be mechanically reused in many contexts, starting with adoption in authoring tools and ensuring compatibility with publishing, production, and archiving workflows.

## Soil

This group came up with concepts for new ways to connect the components of science, these were based on existing schemas (e.g. ActivityPub, JSON-LD, COAR Notify, etc.). High level concepts such as "Federated DataCite" and "Science DNS" that can be resilient to failure as well as include concepts of spam-protection from email services. A concept of **collections and containers** emerged, with new types of research objects that could be composition of other objects, including recognizing the existing role and potential of [MECA](https://www.niso.org/standards-committees/meca). There was also the concept of "an index of indexes", a role that OpenAlex is currently fulfilling in the ecosystem, that connects and exposes research objects in many diverse repositories.

The group proposed architecture that could bring together some of the content from the "bedrock" in new ways to enable composable science in containers that are "in-family" with today's preprints and articles. For example, pulling in tables, or figures from other existing research that was published. There were overlaps identified with the group working on an open exchange architecture and participants ended up joining that group effort.

## Ecosystem

The group discussed the potential for many new types of applications and services that could be built from the new components in the bedrock, especially if they are made more accessible through APIs and services (e.g. OpenAlex, DocMaps) that connect and add meaning through graph-networks (citations, person disambiguation, reviews, etc.). The group talked about new metaphors like "spotify for science" that could be rapidly prototyped to show new curation and trust metrics on the research.

The group proposed to do a sprint using collaborative prototyping and new LLM-based programming tools to quickly pull together concepts and iterate as a group. As not everyone was familiar with these tools, they decided to mostly work together on a single new prototype that brought together aspects of search, discovery, curation, trust signals, and embedded reading experiences from the open exchange architecture. A separate effort was proposed to look at the combination of multiple computational research articles from the NeuroLibre project, to explore what is possible when full context to the science is made available (the environment, data, code and narrative).

Another group discussed the importance of working with scientific communities in understanding needs and interests and creating spaces for agile and iterative deployment and feedback with the groups and people who are sharing science. They discussed the importance of communities coming to tool-builders with their needs and ideas, rather than tools being pushed to communities, and the attributes of forming these community relationships. Personas can be valuable in thinking through user needs, and there was interest in collective personas in scientific communication. 

# Evening Activity & Day 2

We went to an arcade for dinner and some activities and to continue discussing ideas for the second day. Many other connections were made between the various participants.

:::{figure #fig-event} event.png
The sensory experience of the arcade was intense, lots of fun was had at ski-ball, mario, pac-man, and basketball. 👾🕹️
:::

The [second day](./day-2.md) was unstructured time in the San Diego Made Factory, where we hacked, learned, built schemas, talked about approaches, and vibe-coded prototypes for the demo-day on Saturday morning.

:::{card} 🗺️ Day 2 - Building with a Plan
:url: ./day-2.md
The second day was unstructured time in the San Diego Made Factory, where we hacked, learned, built schemas, talked about approaches, and vibe-coded prototypes for the demo-day on Saturday morning.
:::
