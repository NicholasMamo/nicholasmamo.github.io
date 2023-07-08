---
title: "Document-pivot algorithms: a brief introduction"
date: 2020-07-27T12:32:40+02:00
draft: false
tags:
- topic detection and tracking
- twitter
---

Topic Detection and Tracking has been around for more than 20 years, but during this time, there has been a lot of research.
When researchers started creating systems, they went off in a few different directions.
Earlier, I took a [brief look at Topic Detection and Tracking]({{< ref "event-tracking-introduction" >}} "Event tracking: a brief introduction").
In this post I take a look at one of the two main approaches to solving the problem: document-pivot methods.

Picture this: you're out and about when you hear someone say the phrase "free hamburger."
You walk a few paces and you hear that wonderful, magical phrase again: "free hamburger."
Wouldn't you think that someone is giving away hamburgers for free?
That's the intuition behind document-pivot methods in Topic Detection and Tracking.

## Document-pivot and feature-pivot methods

[There are several ways of splitting Topic Detection and Tracking approaches](https://onlinelibrary.wiley.com/doi/full/10.1111/coin.12017?casa_token=Ep-hk09cPSAAAAAA%3AffUJ_MhRr9I3drl6jMoRa1nHtrpYoxTkhAzc5Y4DDbLQ62LqsEbS3Hz28uWbpQjTL8iCptt5CtEXHw):

- Some methods use Twitter, while others use news reports.
- Some follow a specified event, like a football match, while others find breaking news from all over the world.

In this post and the next one, I focus on a different split: the different ways of detecting what happens during an event.

You might be thinking to yourself: there must be an infinite number of ways of detecting what happens during an event.
That may be true, but many of those solutions fit in one of two broad categories: document-pivot and feature-pivot approaches.
Don't let the names intimidate you.

Document-pivot means approaches that revolve around (hence pivot in the name) documents, such as tweets.
Feature-pivot means methods that revolve around features, such as how much users are tweeting at any given moment.
Personally, I prefer to think of them as questions:

- Document-pivot: what are people talking about?
- Feature-pivot: how are people talking?

In this article, I take a look at document-pivot approaches.
These methods are very simple, but they aren't very common because they're limited in other ways, as we'll see.
You can think of these kind of approaches as looking for what subjects users are talking about.
If many people are talking about a goal in a football match, then it's likely that someone must have scored.

## Document-pivot methods: what are people talking about?

Document-pivot methods get their name because they work at the level of documents.
Documents may be news articles, tweets or any other type of text document.
To decide what is happening, document-pivot methods revolve around clustering.

Clustering is a fancy way of saying that the method groups documents together.
The goal of clustering is to get all of the documents that are talking about the subject in one cluster, or group.
At the end, we choose some clusters and call them topics.

On what basis does a machine group together documents?
Usually, on the words in the documents.
If two documents are using the same words, they are probably about the same subject.
In that case, the machine groups them together, but it's not always so simple.
For example, read the following two tweets.

> GOAL!
> 
> That escalated quickly!
> 
> Olivier Giroud makes it two after being played in by Mason Mouint.
> 
> Chelsea 2-0 Wolves 
> 
> — [@BBCSport](https://twitter.com/BBCSport/status/1287414847869681664)

> Like London buses! 🚌🚌
> 
> Chelsea grab their second goal in quick succession - is that Champions League qualification sealed? 🇪🇺
> 
> — [@SkySportsPL](https://twitter.com/SkySportsPL/status/1287416529303277569)

Both tweets describe the same moment when Olivier Giroud, a Chelsea football player, scored against Wolves.
And yet, there is only one word common between the two tweets: _Chelsea_.
The second tweet doesn't even mention who scored!

As a result, it's highly likely that the two tweets would end up in different clusters.
We call that fragmentation, and it is problematic because we needlessly separate the same story into different topics.
We might even report the same thing twice unknowingly.

## How many people are talking about it?

There is another problem with clustering.
How many people must be talking about a story to accept that it really did happen, or that it is interesting?
One person is probably too few, but are three users enough?

[This paper](https://link.springer.com/chapter/10.1007/978-3-319-24027-5_6) requires that at least ten people must be talking about a story to accept it, whereas [this one](https://ieeexplore.ieee.org/abstract/document/6425790) requires 250 Twitter users.
Two hundred and fifty tweets may sound exaggerated, but even getting ten users talking about a story may not be very easy.
As we saw above, tweets on the same subject can still end up in different clusters.
The risk is even greater when using tweets instead of news articles; since tweets are so short, it's less likely they would use the same words!

Another issue is that not all important stories are popular.
In football, goals are more important than substitutions, but that doesn't mean that substitutions aren't important.
The next two tweets will show you just how important substitutions can be.

> A trio of subs - @Mahrez22, @IlkayGuendogan and @fernandinho are on for @ericgm3, Rodrigo and @PhilFoden
> 
> 🔵 2-0 🟡 #ManCity | http://mancity.com
> 
> — [@ManCity](https://twitter.com/ManCity/status/1287418449585672198)

> MAKE THAT FOUR!!!
> 
> 🔵 4-0 🟡 #ManCity | http://mancity.com
> 
> — [@ManCity](https://twitter.com/ManCity/status/1287428122716131333)

Riyad Mahrez didn't start this match, but he came on and scored.
If the timeline tells you only that Mahrez scored, you might be confused.
If he wasn't playing, how could he score?
However, substitutions have few likes and retweets because they aren't as important as goals.
As a result, they might create small clusters that we end up discarding.

In other cases, the event itself may be unpopular.
If very few people are watching—or tweeting about—a football match, then all clusters will be very small.
In that case, the timeline might end up looking very empty.

## Does popular mean important?

That's not the end of the problems either.
So far, we have assumed that if people are talking about something, then it is important.
That is a reasonable assumption, but that doesn't mean it's always true.

For example, this tweet is about Andros Townsend, a Crystal Palace player, running into and knocking over a photographer.
It is certainly amusing (if you're not the photographer), but whether that is an important part of the football match is debatable.

> Back at Selhurst Park against Chelsea, Townsend ran into a photographer knocking her over, before checking she is OK and then chasing after the ball.
> Not something you see everyday.
> 
> — [@bestgug](https://twitter.com/bestgug/status/1079461099798327296)

Another common aspect of Twitter is opinion.
Many people might share the same opinion, but opinions are subjective and, as a result, rarely newsworthy.

Working out which clusters do not represent an important story and filtering them requires more work.
That is why document-pivot approaches are relatively uncommon in Topic Detection and Tracking, even though they are very simple.

In the next post, I will take a look at the other type of approaches: feature-pivot methods.
These approaches come with their own limitations, but they are much more flexible.
As a result, they are far more common than document-pivot methods.
By now, you can start to appreciate that Topic Detection and Tracking is not as straightforward as it seems… especially when working with tweets.

## Reading

If you want to learn more about Topic Detection and Tracking and document-pivot methods, these papers from this article will get you started:

- [Real-Time Entity-Based Event Detection for Twitter](https://link.springer.com/chapter/10.1007/978-3-319-24027-5_6): a paper that uses clustering to detect breaking news around the world.
- [Semantic Expansion of Tweet Contents for Enhanced Event Detection in Twitter](https://ieeexplore.ieee.org/abstract/document/6425790): a paper that uses clustering to detect news stories from Turkey, and which requires 250 people to be talking about an event to accept the story!
- [A Survey of Techniques for Event Detection in Twitter](https://onlinelibrary.wiley.com/doi/full/10.1111/coin.12017?casa_token=Ep-hk09cPSAAAAAA%3AffUJ_MhRr9I3drl6jMoRa1nHtrpYoxTkhAzc5Y4DDbLQ62LqsEbS3Hz28uWbpQjTL8iCptt5CtEXHw): a survey that explores different ways of approaching Topic Detection and Tracking in Twitter.
Interested in learning more? In the next post, I explain the intuition behind the other popular type of Topic Detection and Tracking approaches: feature-pivot methods.