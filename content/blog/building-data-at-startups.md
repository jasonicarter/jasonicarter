---
title: "Buliding Data"
description: "As a data solutions strategist for startup companies, there's only one way to build data. Fail and repeat."
tags: [
    "data",
    "startup",
    "analytics",
    "data infrastructure",
    "data engineering"
]
date: "2019-04-26"
---

## Infrastructure, Trust, Appreciation and Decisions

> failure (fālˈyər)
>
> n. The conditioon or fact of not achieving the desired end or ends:
> the failures of an experiment

***

## I’ve failed

As the first [Data Engineer](https://www.cio.com/article/3292983/what-is-a-data-engineer.html) at a startup in Toronto I had lofty goals, great new-ish/slightly borrowed ideas, and I even had _phases_ so everything would fit nicely into my grand plan. Don’t get me wrong, failure isn’t a bad thing, and I got plenty of shit done. But I knew the problems, I knew the solutions, I had everything grouped in phases. How could I fail? How did I???

Lets start from the beginning, Day 0, I thought long and hard about what I wanted to accomplish and how I’d do it, so lets start there. Lets democratize data!

**Phase 1** would see the removal or update to legacy event tracking goal and replaced with consolidated 3rd party APIs from [segment.com](http://segment.com). I would Keep everything else as untouched as possible and build anew in parallel since business needs can’t take a backseat to greatness.

**Phase 2** is where the modern serverless data infrastructure was born. I would use the latest and greatest data technologies, everything open source and maybe even some “bleeding edge” alpha shit to make a fool(and future) proof infrastructure. This would provide us with all the scalability we could ever foresee, while also allowing for analysts and data scientists to _access, discover and build actionable insights_ ← one of those ideas I borrowed.

**Phase 3** wait for it…Self-serve. Need I say more? Any talk about data engineering, data culture or data-driven decision making, isn’t complete without the dream of a self-serve reporting BI platform where every employee knows, uses and loves SQL.

**Phase 4** data products, both internal and external facing. The data team should not only facilitate providing data that is easily accessible and discoverable, but also, particularly at a small company, should drive things such as an A/B Experimentation Platform, Data Science workflows, Data APIs for the product team to hook into and an official home for all data related documentation across the organization such as [Airbnb’s Knowledge Repo](https://github.com/airbnb/knowledge-repo).

![](https://cdn-images-1.medium.com/max/600/0*oqXyKt05uwdmNkd8)

Photo by [Brooke Cagle](https://unsplash.com/@brookecagle?utm_source=medium&utm_medium=referral) on [Unsplash](https://unsplash.com?utm_source=medium&utm_medium=referral)

Mixed in with all of that were lunch-n-learns, data surveys, best/better practices for making data-driven decisions, etc etc. Your basic [data-university-within-the-company](https://medium.com/airbnb-engineering/how-airbnb-democratizes-data-science-with-data-university-3eccc71e073a) approach.

I failed. Not only did I _fail fast and fail often_, but also, I often failed pretty slowly, grinding it out trying to understand what was happening before my eyes.

* * *

Today, I’d like to write a little story about what I’ve experienced personally across my data career and what I’ve learned by reading stories from others across Medium. And maybe at the same time I’ll come up with what I would have done differently.

Data Engineers, in theory, aren’t responsible for “everything data” at an organization. There’s no one liner in the default role description across the internet which states

> Data engineers collect, transform and publish data enabling data driven decisions at an organization…ALSO they create, maintain and evangelize the data culture we all know, love and want.

But in quite a number of cases, particularly in early stage “data maturity” companies, this is the requirement whether or not the employee or employer know it.

**Data culture** is something you hear about A LOT and personally I’m a strong proponent for a top-down approach to data culture, meaning, if your CEO isn’t into it and doesn’t demand data-backed results from his direct reports, you’ll have no luck getting anyone else to care about a data driven culture.

But in most startups, at least from what I can tell, this seems to be the case. Primarily because small companies either have one maybe two “data people” so any data related responsibilities get shifted away from everyone else and onto the data people. In early stage data maturity companies, particularly startups, the first data engineer will almost always have to take on the role of promoting data knowledge and enthusiasm at the company along with the normal expected data engineering stuff.

For better or worse, this is what happens and instead of arguing about how to fix it, I want to write about my experience of dealing with it. I’m currently a Data Engineer, but I’ve had multiple Data Analyst and Software Developer roles across enterprise and startup companies. And in each new role, the scientist part of my brain, always wanting proof, made me the data person at ever company or team I was apart of.

Nurturing a data culture was something I found quite exciting when I first joined my current company. The idea of building something new, not just the infrastructure, that in some way would direct the overall data strategy at the company was thrilling. But how do I create this data culture? Can we define it? The internet gives you the sense of _data culture_ to be a single, cut-from-solid-metal intricate mould, where looking directly at it defies all understanding of how anything so complex can be the creation of mere humans.

But for me, a data culture is a catch all umbrella, which for clarity sake, I’d like to split out and group into 4 sections. My own personal catch all mini-umbrellas. And this is where the story begins about my opinion and experience on **Building Data**.

![](https://cdn-images-1.medium.com/max/800/0*Ng-zfOvRWGpvuHJo)

Photo by [Stephen Dawson](https://unsplash.com/@srd844?utm_source=medium&utm_medium=referral) on [Unsplash](https://unsplash.com?utm_source=medium&utm_medium=referral)

* * *

### 1\. Building Data Infrastructure

Every company seems to want or need a Data Engineer these days. What this person does for the company varies to a large degree depending on the industry and data maturity of the company. This can span across startups to large been-around-forever type enterprise companies.

My primary role was to fix problems, support people and build an infrastructure. But not in so few words, it was more like

> To simplify, consolidate, manage, maintain and provide reliable data to all stakeholders within the organization, but first fix, remove and/or replace what’s not working — A typical startup Data Engineering need

The concept is pretty straight forward but there’s always a gotcha and one of the them is to remember the company still has to function while you’re tolling away building infrastructure. Meaning, the company’s current and short term needs must still be supported, stakeholders still need metrics to view and BI analysts still need dashboards and charts to analyze. This is where ridiculously good priority skills, multi-tasking skills, communication and expectation management skills come into play. If you have none of those, then becoming the first (or one of the first) data engineers at your company was probably a bad idea for you and your company.

A close second to the “gotcha” list, is how hard it is to fight want vs need and the real need to balance building for the future but not the distant future. Unless you’re specifically a “data” company, or perhaps an IOT company, your first foray with a data infrastructure shouldn’t be the much hyped [data lake](https://en.wikipedia.org/wiki/Data_lake). This applies to your data tools as well, I’m looking at you [Looker](https://looker.com/). Think baby steps or perhaps not baby steps but toddler size steps. There’s no need to spin up a [kubernetes](https://kubernetes.io/) cluster to run your two Python scripts in [Docker](https://www.docker.com/) containers. But that doesn’t mean your infrastructure starts with cron running on a server under your desk.

A good, simple and typical starter batch processing infrastructure may look like AWS S3, Redshift, Airflow on EC2/hosted (or AWS Glue) and your BI tool(s) of choice. You may also want to add on a monitoring stack, be it Prom+Grafana or just AWS CloudWatch. With this setup you can easily scale up and out, replace parts or move the whole thing to another provider (limited vendor lock-in). You can also easily add on workflow tools for the Data Scientists or Data Analysts, which at this point, your company probably doesn’t have yet. And a company with their first data engineer is now probably expecting some _data democratization_ to happen (that’s “synergy” between data and democracy for those not in the know) and with that comes the much hyped **self-serve** BI platform/analysis tools.

The phrase “self-serve” is like fools’ gold or perhaps a pet snake or [the scorpion and the frog](https://en.wikipedia.org/wiki/The_Scorpion_and_the_Frog), basically anything that looks great at first and then bits you in the ass the first chance it gets.

![](https://upload.wikimedia.org/wikipedia/commons/7/79/Tortoise_and_Scorpion.jpg)

Self-serve BI, aka democratizing data, is when someone imagines a world where tools with intuitive drag-n-drop interfaces are actually intuitive for all, people only ask questions they can’t answer themselves and everyone knows SQL. Users who do excel would have most likely done so with any tool provided the right resources were available to help. These are users who are enthusiastic to learn more about the tool and data, and don’t mind the learning curve associated with the reward. However, in reality, creating a self-serve analysis environment gives you a mixed bag of mass confusion, greatness and stupidity such as

1.  Users who think the old way of Google Sheets was better
2.  A lot of great new questions are asked
3.  A lot of not-so-great already asked questions are asked
4.  Everyone hates SQL. Everyone
5.  Explaining how drag-n-drop interfaces work

Self-serve will overwhelm you and underwhelm your stakeholders. If you’re not prepared with a lot resources — people to help, documentation, time to kill — this venture will kill any productivity you had as a data engineer, and maybe even your soul. You’ll be much better off working closely with one or two key members of other teams, helping them learn the new systems, and discover the data, letting these semi-data people help work directly within their own teams then opening up the flood gates know as self-serve BI environment later down the road.

* * *

### 2\. Building Data Trust

If no one trusts the data you’re providing, it’s not worth providing it. I learned quickly that a semi-great looking infrastructure spitting out data isn’t enough. People need to use that data to view results and gain insights into anything from marketing campaigns and conversion rates to A/B experiments and user in-app behaviour. If your end users simply don’t believe the metrics you’re providing, they’ll quickly stop using your data. And if you’re lucky, they’ll at least tell you that they don’t trust the data— and yes, that’s being lucky. The only thing worse than end users not trusting your data, is users who don’t trust your data, stop using it, find alternatives and never tell you about it.

Single (one) source of truth is a good way to isolate the good and the bad when it comes to data trust.

> In [information systems](https://en.wikipedia.org/wiki/Information_systems "Information systems") design and theory, **single source of truth** (**SSOT**) is the practice of structuring information models and associated [data schema](https://en.wikipedia.org/wiki/Database_schema "Database schema") such that every data element is stored exactly once. Any possible linkages to this data element (possibly in other areas of the relational schema or even in distant [federated databases](https://en.wikipedia.org/wiki/Federated_database "Federated database")) are by [reference](https://en.wikipedia.org/wiki/Reference_%28computer_science%29 "Reference (computer science)") only —[ Wikipedia](https://en.wikipedia.org/wiki/Single_source_of_truth)

In English, and in context, having your metrics rely on one table or process gives you two great things 1) single point of failure but also a single point for fixing that failure and 2) if the metric is wrong, everyone using that metric is wrong by the same degree.

I think my first point is pretty simple to understand and appreciate. If something breaks, like it inevitable will, it can only break in one place and you’ll only need to fix that one place to get every downstream process and report using the correct metric again. But let me dive into point two(2) a bit as no one likes getting wrong data but it sounds like I’m saying that’s a good thing. I’m not. I’m saying it’s a good thing that _everyone is wrong_ _by the same degree_. In my experience, one of the worse things that can happen to have a working pipeline processing data incorrectly; however, worse than that, is having downstream processes and reports requiring the same metric but having **different** wrong answers. When you realize the problem, it’s one of those times where you sit silently staring at the screen, take a deep slow breathe in and out, then say “Shit. That’s not good”. And that’s were SSOT comes in. You can use different data sources, transform and wrangle your data together but in the end if your metric is using one table, set of tables or process as its base, and all other processes utilizing its output as their own base, you will never get a metric giving a different wrong answer across pipelines.

Hard to believe but this all goes back to data trust. If stakeholders don’t have or lose their trust in the data, it’s hard to bring it back. SSOT helps prevent that from happening, so spending a lot of time here would be well worth it for any data engineer but particularly one who’s entrusted with building a culture reliant on data.

* * *

### 3\. Building Data Appreciation

Appreciation. Not in the sense of needing people to appreciate the work you do but the data itself and how they can use it to achieve their own goals. Data appreciation needs to fostered among team members and the company as a whole, without this a — so what? — attitude will always get in the way of people utilizing everything you’ve provided.

> If a data engineer creates discover-able, reliable, trustworthy data-marts but end users don’t gives a shit, was the data engineer really successful?

This is probably more of a company culture topic but if you’re given tools to help you succeed in your role would, you use them? This is where data appreciation comes in, where your end users care about what you’re doing and more importantly they care about why you’re doing it. You and your infrastructure exist for one reason — provide business insights, either directly or indirectly, your infrastructure must facilitate this. If users can’t, voluntarily or by other means, appreciate those wide dimension tables or those time-series metrics you’ve painstakingly provided, you serve no purpose. Period.

At a startup (or any company at an early stage of data maturity), your role as a Data Engineer probably means you have to not only build an infrastructure but also build this “appreciation” for data, to evangelize data within and throughout the organization. Failing to do this efficiently would result in your own overall job failure. **Build it and they will use it**,  does not apply here.

* * *

### 4\. Building Data (driven) Decisions

Data driven decisions or any iteration of this theme is basically the concept of business users utilizing data insights to make, verify and/or validate their decisions, before they action them. These decisions could be the foundation of a hypothesis for an experiment or an explanation of a failed marketing campaign or the reason to invest in a particular product feature. The point being, you rely on data to help you make decisions, this facilitates a more efficient process and allows you to work on things that matter, things that bring value to you and your organization.

While many people love the notion of data driven decisions and beg for more data, others push back. It’s natural wanting to keep doing what you’re use it, I myself do it from time to time which is why I mentioned earlier that I’m a strong proponent to the top-down approach of data culture and here’s why — imagine you’re a Sr. Manager of a feature team who just deployed a great new feature into your amazing product. Answer these questions for me

1.  How many customers using your cool new feature?
2.  What’s the frequency at which your feature is being used?
3.  Are you going to build cool feature v2?

Pretty simple questions that you could probably guess at with a big YES to Q3, because why wouldn’t you fix a few bugs and enhance a few things to a feature that’s already in production? But what if your boss, in a great top-down fashion, demands that any decision you present to her must come backed with data? Now you have a whole set of new questions like, _“did I even instrument this new feature to capture the data required to answer the questions?”_ or maybe _“why is the data showing me very few customers are actually using the feature but my gut tells me doing great?”_. Version 2 is going to be a tad bit hard to justify now that v1 has no data supporting its success.

Many more questions and insights, both good and bad, come when you’re referencing data but none of that is possible if the data driven culture doesn’t come from the top down. You’re either pumped about getting your hands on data, or you’re not. And if you’re not, it’s just too easy to ignore the extra effort required unless you’re gently pushed into the right direction.

And although you’re not the person _making_ those data driven decisions, we’re talking about a situation where you’re the only data person at the company and everything data related falls onto your shoulders. And this is probably **the hardest (and most important) part of the role** at any company when you’re building data.

![](https://cdn-images-1.medium.com/max/800/0*Uur0bBKAMVy_S2JX)

Photo by [Franki Chamaki](https://unsplash.com/@franki?utm_source=medium&utm_medium=referral) on [Unsplash](https://unsplash.com?utm_source=medium&utm_medium=referral)

* * *

## Building A Conclusion

As a story about building data, you might have had the impression or anticipation for some technical diagrams, an example Airflow DAG code block somewhere or at least some pseudo code. But I think all of those things come and go. Either the industry changes, the role description changes or more often than not, the technology, process and technique changes. Plus, there are PLENTY of Medium stories out there already talking about how to build a data infrastructure, or how to use Airflow with K8s.

For me, and in the context of this story, building data is a lot more than just the tech stack X for company Y at startup stage Z. At some stage of a  
company’s life, they need their first employee to help code a new feature, first IT guy help provision all those new laptops, first HR member and somewhere down the line, their first data person. That data person, the first real full-time data person, the data engineer, will inevitably have do more than just write a couple of cron jobs, python scripts and connect the dots from one tool to another. In order to not fail, that person will need to build a data infrastructure, she’ll need to build trust between end users and the data she provides, she’ll need to build user’s appreciation for the tools they have and the data that can facilitate them reaching company goals, she’ll need to build a data driven decision making mindset among her peers. And as _the_ data person, as the Data Engineer, all of this is encapsulated into her role, all of this is encapsulated into creating a data culture at a company that starts from zero. All of this encapsulated into **building data**.

By [Jason I. Carter](https://medium.com/@jasonicarter) on [April 26, 2019](https://medium.com/p/23d598f57ab7).

[Canonical link](https://medium.com/@jasonicarter/building-data-23d598f57ab7)