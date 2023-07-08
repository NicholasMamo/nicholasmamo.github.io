---
title: "A requiem for Twitter: what science has lost"
date: 2023-07-02T11:19:29+02:00
draft: false
tags:
- twitter
- opinion
---

Twitter is dead.
Technically, it is still alive—barely—but for scientific research, it is as good as dead.
Twitter's demise did not start with the saturation of blue ticks, nor with [the nonsensical limits on daily views](https://mastodon.social/@memonick/110640399936057197).
It started and ended with cordoning off access to the Twitter API; now, it costs $5,000 per month for 1,000,000 tweets—a tenth of what academics previously got for free.

I started [researching on Twitter]({{< ref "/posts/about-events" >}} "About events") in 2016.
As an undergraduate in my final year, I had to come up with a project, and I decided to build a news detection algorithm.
It felt natural and inevitable that I would choose Twitter—grand, open Twitter.
I graduated, started and completed my postgraduate and doctoral research, and I never strayed far from Twitter.

To my mind, Twitter had—and still has, in inaccessible corners—everything that I needed.
Twitter was open with its data, in ways that few other privately-held social networks were back then, or have been since.
Above all, it had volume and velocity.
Not that Twitter could rival Facebook, of course, but it had enough volume and velocity to power my algorithms, and the company valued academics.

No one forced Twitter to favor academia, but it did, in direct contrast with what happened since Elon Musk took over.
In 2020, at the beginning of a migration to a new API version, Twitter asked to speak with academics.
The social network actively sought out the conversation to placate our fears.
I volunteered, and the one-hour interview revolved entirely around what _we_, as academics, needed from the API.
The new API brought slightly more stringent limits than before, but it remained open, with far more generous limits than those of commercial entities.

Of course, Twitter has always felt coarse, by nature or design.
The short length of tweets limited (but concentrated) information, and the information, often from anonymous accounts, was noisy, spammy or just mundane.
In a way, however, the same crudity attracted me and many others to Twitter.
Twitter afforded us a glimpse into an unfiltered version of everyday society.

Twitter's demise might generate a sense of morbid thrill, but science stands to lose a lot.
By extension, every one of us stands to lose a lot.
In the rest of this blog post, I outline some of what Twitter's changes mean to academic research.
I will focus only on the applications to which my research area (event tracking) and adjacent fields exposed me.
Therefore, do not expect a full course but a sharp taste of what science has lost.

## Twitter, the public town square

It feels cliché-d, and wrong to say it now that it has been co-opted and twisted by Musk, but Twitter really felt like the public town square.
Public figures—brands, politicians and journalists, in particular—congregated on Twitter, not larger social networks, because the social network felt like a public town square.
For many public figures, Twitter became the means of communication, even when you least expected it; [the Royal Family announced the death of Queen Elizabeth II on Twitter first](https://twitter.com/RoyalFamily/status/1567928275913121792).

Evidently, the voices of public figures drowned those of more normal citizens, but our voices remained public and free.
So much so, in fact, that the Arab Spring received the label of the Twitter or Internet Revolution.
The label has been thoroughly debunked: [social media was a coordinator, not an instigator](https://onlinelibrary.wiley.com/doi/abs/10.1111/dome.12076); [a tool to aid social movement, not the social movement itself](https://www.tandfonline.com/doi/abs/10.1080/14747731.2011.621287).
Nevertheles, while Twitter did not precipitate the unrest, it served a purpose.
It served as a form of new media that dictators could not silence.

Of course, the users and their voices will remain on Twitter.
(The ears will not necessarily remain, though; if the limit on tweet views remains, then who will hear the voice?)
What will not remain, however, are the scientists to make sense of the voices.
We would not have known, today, the extent to which Twitter and social media contributed to events like the Arab Spring.
At best, we would have to contact people on the ground, a much slower and more expensive process.

## Twitter, the news capital

Beyond a sociological interest, Twitter as the public town square had another appeal, the same one that attracted me to the social network in the first place.
Twitter became the capital of news: regular users acted as citizen journalists, citizen journalists attracted professional journalists, and professional journalists attracted more and more regular users.

In 2017, [Reuters estimated that between 10% and 20% of all news broke on Twitter first](https://ieeexplore.ieee.org/abstract/document/8258082/).
[Twitter leads the news media in breaking news from live and unplanned events](https://ojs.aaai.org/index.php/ICWSM/article/view/14450), like sports and natural disasters.
Twitter broke news about the deaths of [Osama bin Laden](https://dl.acm.org/doi/abs/10.1145/2207676.2208672) and [Michael Jackson](https://dl.acm.org/doi/abs/10.1145/1653771.1653781), and news of [the Baston Marathon bombing](https://journals.sagepub.com/doi/abs/10.1177/0739532916648961).

The 10–20% estimate, which has probably gone up since 2017, represents the tip of the metaphorical iceberg.
In addition to the news that breaks on Twitter first, much more spreads there.
No other social network seems capable of matching Twitter on the speed of news dissemination.
The morning of 24 February, 2022, as Russia invaded Ukraine, Twitter served as my go-to source for news.
It was not juts me; the Reuters Institute for the Study of Journalism immediately tweeted [a selection of live threads](https://twitter.com/risj_oxford/status/1496788302527086594) and [a list of journalists reporting about the war on Twitter](https://twitter.com/risj_oxford/status/1496791970965975045).
Twitter became the newswire, a bustling and noisy newswire.

To deal with the information overload, Artificial Intelligence turned to Twitter, and inversely, [Twitter users turned to Artificial Intelligence]({{< ref "event-tracking-introduction" >}} "Introduction to event tracking").
When journalists and newsrooms could not cope with Twitter's volume and velocity, and noise, they turned to science and academia.
Algorithms like [Reuters Tracer](https://ieeexplore.ieee.org/abstract/document/8258082/) helped discover breaking news automatically.
Today, we also use event tracking algorithms, like Reuters Tracer, to [follow live events, such as football matches](https://www.researchgate.net/publication/355765864_Fine-grained_Topic_Detection_and_Tracking_on_Twitter).

Twitter's utility to AI and news extends beyond event tracking.
In 2022, for example, the [JournalismAI initiative](https://www.lse.ac.uk/media-and-communications/polis/JournalismAI), which promotes the use of AI in newsrooms (also known as computational journalism), held fellowships.
One such project, [Parrot](https://parrot.report/), studied how disinformation and misinformation spreads.
Almost by default, the researchers turned to Twitter.

## Twitter, the emergency hotline

The speed of news dissemination served another purpose: gathering situational information.
Situational information is any information that directs first respondents to wherever help is needed during emergencies, such as natural disasters, health emergencies or terrorist attacks.
Once again, to cope with Twitter's momentous volume, science used event tracking algorithms for a variety of tasks, including [to detect earthquakes and send warnings about secondary waves](https://dl.acm.org/doi/abs/10.1145/1772690.1772777).

Twitter can contribute to future emergencies, not just current emergencies.
[In 2021, researchers working on old datasets found that cases of pneumonia spiked in areas that would later become hot-spots of COVID-19 infections](https://www.nature.com/articles/s41598-021-81333-1).
The spikes happened weeks before the first officially-announced cases of COVID-19.
In other words, they detected signs of COVID-19 before it had become a pandemic.

---

All of that lies in the past.

Twitter's restrictions have blunted our ability to do journalism and science: to research public sentiment, to detect the news and handle or prepare for emergencies.
You could blame politicians and journalists for relying too much on Twitter, even while Twitter plays its swan song, but they went where the people were.
You could blame scientists for depending on Twitter, but we also went where the data was.

Scientific research will obviously survive.
Artificial Intelligence research will reinvent itself to understand society, to make sense of the news and to aid in emergency relief efforts.
I plan on writing more about how we could replace Twitter with other social networks and data sources; moving away from Twitter is, after all, what I have had to do.
But it will take time for the scientific community to reinvent itself, and until it does, we have lost Twitter, and the people and the data, and the science.