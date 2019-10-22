+++
title = "After Deep Learning: 4 Months a Data Engineer at Format"
description = ""
tags = [
    "data",
    "startup",
    "analytics",
    "deep learning"
]
date = "2017-12-27"
categories = [
    "Development",
]
+++

> Everyone has a plan until they get punched in the face.
> \- Mike Tyson

#### The Beginning of 2017

My career punch in the face was more like repeated body blows which lead me to here, my end of year recap, 2017.

If you’ve been keeping track, approximately 8 months ago, after those repeated body blows telling me I wasn’t on a career path I loved, I quit my job and started on my self-pace [Machine and Deep Learning study schedule](https://towardsdatascience.com/4-months-of-machine-deep-learning-89f6ab56a2fd). In late July I started my job hunt, and since accepting a position at [Format](https://www.format.com) I’ve been working non-stop, loving what I do, the people I do it with and the [community](https://www.format.com/magazine) I do it for.

But let’s take a step back. After taking this journey (and writing about it) I feel an obligation, and a need, to tell you a little about my job hunt, why I chose Format, what I do now, and what the future holds for me.

* * *

#### The Job Hunt

After my 4 months of studying and side projects, I felt that I had a pretty decent understanding of not only the main fundamentals of Deep Learning but more importantly the practical application of the techniques. Some companies thought so as well, while others not so much.

The companies I applied to could be categorized into three groups, small/startups, medium and large companies. I’ll explain a little more about these three groups but first let get some numbers out there: Applied to: 19; Interviewed with: 7; Declined to continue with: 2; Accepted: 1

The two companies I declined to continue the interview process with were purely because I didn’t believe the fit was right.

However, some companies responded with an automated email and link, asking me to take a test. I ignored their requests. Sorry, but if you don’t have the time to at least have someone actually write an email or call, why should I take your test??? Not out of principle but out of decency. Think to yourself, do you want to work for a company which treats its potential employees with an automated…

> Hello, I didn’t bother to read your resume and I don’t care that I made you fill out our long online application form with questions like, “tell me what makes you unique”. Instead, prove you’re worth my time, go do this project on YOUR time and get back to me.

No. I will not get back to you.

#### Startup vs Medium vs Enterprise

Does size matter? I found the larger the company, the more specialized or narrow your focus will be. For example, I interviewed for some medium/large companies who saw me fitting in best as a data analyst, while other smaller companies thought I would be perfect in a machine learning engineer role. Also, in larger companies you can expect more of a mentorship/learning experience but the smaller the company the more you’ll have to figure things out for yourself. _Learn by doing, failing and repeating_. You need to know yourself, what you’ll enjoy doing but also where you want to be 5 or 10 years down the road.

So here’s my piece of advice: Don’t assume the job roles in Machine/Deep learning will carry the title by name. Read the job description and you may be pleasantly surprised, like I was, that many companies want a machine/deep learning engineers — they just want you to do other things as well.

* * *

#### Format

A Toronto based, bootstrap startup, helping artists showcase their work professionally and beautifully on their own online portfolios, designed for the creative mind.

Like a typical startup bootstrap company, Format needs people with multiple talents. And as such, the Data Engineer role I applied for was really _part_ _Data Engineer, part Data Analyst and part Machine Learning Engineer_. Am I great at all 3 roles? Hell no! But my past experience, self-study machine/deep learning work, willingness and ability to pickup new technologies, made me a perfect fit (in my opinion). And it was actually that mixture of roles that had me so excited to join the company, but it didn’t stop there. Unlike a lot of other companies I interviewed with, Format had long term plans for the role which included becoming the evangelist for a company wanting to become a data-driven organization.

#### My Current Work

When a company decides it needs a data team they probably start to break things down into steps and roles, trying to figure out how many people are required and in which roles. To many, it looks like this:

1.  Data Collection (Developers)
2.  Data Storage (Data Infrastructure Team)
3.  Data Analysis (Data Analytics/Data Science Team)
4.  Data-Driven Decisions (Managers)

Ignoring the managers, you need 3 teams of people but at a minimum, you might have a single person for each team:

1.  A data engineer, who can fit in with your developers in terms of engineering skills.
2.  A data analyst, who knows SQL and Python or R. And someone who can understand, or at least appreciate, the actual business side of the company.

The third person I rolled up into data engineer because, if you don’t know or if you can’t learn some basic data infrastructure technologies, can you really call yourself a data engineer???

However, when you’re small and in the early stages of gathering and utilizing your data, it’s possible to get away with only one hire, like myself, a data team of one. I’m heavily involved in steps 1 through 3, and as a company starting its journey to become a data-driven organization, you’ll be relying on every person in each department becoming their own data analyst. This in turn, lightens my load a bit, at least in the early stages of utilizing your data.

#### What I Actually Do

Two weeks in, I made my first prod deployment…in Ruby, a language I learned at Format. Many hats.

And as the Data Team of One, my first job is data consistency, second is to facilitate and evangelize the use of data throughout the company aka turn Format into a data-driven organization. This also means I can’t spend every day building in-house tools with Apache software. Which leads me to my third job, implementing the right tools for the business and not the coolest, newest tech just for the sake of personal enjoyment.

Here’s the high level rundown of the technology I actually use every day:

*   Ruby on Rails
*   [Serverless](https://en.wikipedia.org/wiki/Serverless_computing) data infrastructure
*   [Terraform](https://www.terraform.io/)
*   [Amazon Redshift](https://en.wikipedia.org/wiki/Amazon_Redshift)
*   SQL clients
*   User event tracking tools
*   Marketing and Product analytics tools
*   Word editor

I can’t chat about every single technology we currently use but here’s a quick paragraph:

A serverless data infrastructure lets me focus on the data and not performance or scalability or uptime, etc etc. And to deploy this tech, we use Terraform to codify the environment allowing me to bring up and tear down a new server with predictability. A SQL client is used so we can poke our heads into the raw data which we feed into Redshift from our centralized user event tracking tools. But for the typical user, we have marketing and product analytics tools specialized for their needs such as allowing them to easily create and understand conversion funnels from campaigns or newly deployed feature usages. And of course, a word editor, because _if you don’t write documentation you will become the documentation_. Avoid making yourself a bottleneck.

Noticed there isn’t any Python, K-Means or CNNs listed? Neural networks and machine learning algorithms can do wonders for any business, but if you have inconsistent data, teammates who can’t find the data they need, or worse, a team who doesn’t know how to use the data you provide them, then your cool new bleeding edge algorithms don’t do shit!

#### Future at Format

Data infrastructure work never ends, I always seem to find something more to add, remove or refactor; However, building a serverless infrastructure does help a lot. And as Format moves towards becoming a more data-driven organization — i.e. each department doing their own data analysis, running and analyzing A/B tests on a monthly basis, etc, it pulls me further away from being the analytics bottle neck. This allows me to focus on other random and exciting long term projects like:

*   Building data analytics tools for our customers, helping her to better understand how visitors interact with her portfolio and [online store](https://www.format.com/features/store)
*   Helping our customers organize their portfolio images by categorizing them via CNNs (in-house or otherwise) for automated sorting, collections or recommended tags
*   Utilizing clustering algorithms to group our customers into professions (model, photographer, illustrator, etc) allowing us to tailor their on-boarding experience more uniquely

The potential is endless.

* * *

#### The End of 2017

When I started the year, I wasn’t stuck but tired, of my career direction. I saw Deep/Machine Learning Engineer as a role in its infancy, with a lot of growth into the future. Many of the exciting things happening in this field is in research and not actual implementation and everyday use for businesses. And that’s where I wanted to fit in. Not the Data Scientist but the Engineer. Making use of, implementing and maintaining the technology to help the business and its users.

At [Format](https://www.format.com), I get to do all of that and more. An independent community of artists. An independent company. An exciting and perfect end to 2017.

By [Jason I. Carter](https://medium.com/@jasonicarter) on [December 27, 2017](https://medium.com/p/1c43731bc489).

[Canonical link](https://medium.com/@jasonicarter/after-deep-learning-4-months-a-data-engineer-at-format-1c43731bc489)

Exported from [Medium](https://medium.com) on October 19, 2019.