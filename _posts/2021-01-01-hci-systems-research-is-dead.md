---
layout: post
title: HCI Systems Research Is Dead (Work in Progress)
author: Steven Jeuris
author_website: https://whatheco.de/
---

My apologies for the clickbait. Let me rephrase: _at least to me_, [Human-Computer Interaction (HCI) systems research is dead](http://socratrees.wiki/statement/details/1326). In this article, I share my experience doing systems research and rationale for leaving academia for industry after five years of being a postdoc.

**What's up with the leaves?** You will notice strong claims in this article, such as the one above, link to a website for argumentation called Socratrees. I [welcome you to sign up for private beta](https://socratrees.azurewebsites.net/authenticate/register) and engage with my arguments there to show how foolish they are. You can comment on specific claims I make in this blog post, express agreement by clicking the droplet, or even better, provide counter arguments. Socratrees is one example of what I call "systems research" and will play a crucial role in this story.

## What Is Systems Research?

[UIST recognizes "systems" as a specific type of contribution](https://uist.acm.org/uist2019/author-guide/) and cites [Levin and Redell (1983)][1] and [Olsen (2007)][2] for guidelines to authors and reviewers of such papers.

> It presents a real system, either by a global survey of an entire system or by a selective examination of specific themes embodied in the system. — [Levin & Redell, 1983][1]

Considering how to evaluate "real" _user interface systems_, Olsen states that ...

> [c]omplex systems [generally do not yield to simple controlled experimentation](http://socratrees.wiki/statement/details/1340). This is mostly due to the fact that [good systems deal in complexity](http://socratrees.wiki/statement/details/1343) and [complexity confounds controlled experimentation](http://socratrees.wiki/statement/details/1344). — [Olsen, 2007][2]

Similarly, a Communications of ACM blog post on ["What Makes a Good HCI Systems Paper"][3] by Tessa Lau states:

> Systems often try to solve a novel problem for which there was no previous approach. The value of these systems might not be quantified until they are deployed in the field and evaluated with large numbers of actual users. Yet doing such evaluation incurs a significant amount of time and engineering work, [particularly compared to non-systems papers](http://socratrees.wiki/statement/details/985).

Building complex systems to be used in a novel real-world setting—as opposed to in a highly controlled study—not only [complicates evaluation](http://socratrees.wiki/statement/details/1340) but [also _implementation_](http://socratrees.wiki/statement/details/977).
[Existing software architectures often do not support the envisioned user operations](http://socratrees.wiki/statement/details/1523), requiring [a new software architecture to be built](http://socratrees.wiki/statement/details/1522).
Furthermore, [given that a new system never replaces _all_ existing functionality](http://socratrees.wiki/statement/details/1528), the new software architecture needs to [integrate with existing systems in cases where users rely on them](http://socratrees.wiki/statement/details/1525).

Systems should thus be seen a specific type of "artifact contribution" in HCI which is different in nature from other artifact contributions such as new input and interaction techniques ([Wobbrock & Kient, 2016][4]).

## A Narrower Definition of Systems Research

While accurate, I find that these overly broad descriptions of systems research do not get to the heart of what frustrates many, whom I will be citing in this article, hoping to contribute to this topic in HCI.
Should [any novel real application be considered systems research](http://socratrees.wiki/statement/details/1529?inverse=true)? Should [trivial modifications to existing systems be considered systems research](http://socratrees.wiki/statement/details/1530?inverse=true)? I think not.

Outside of HCI, [Rob Pike](https://en.wikipedia.org/wiki/Rob_Pike), known for his work on UTF-8 and the Go programming language, refers to "systems" as operating systems, languages, or more generally "the things that connect programs together" ([Pike R., 2000][8]).
In this broader context, one could thus view HCI systems as **user interfaces that connect applications together**.

It is [the interplay between software architecture and the novel cross-application user interactions it enables](http://socratrees.wiki/statement/details/1531) which, to me, sets HCI systems research apart from mere "applications". Often, systems research tries to _reimagine_ what an "application" is. Two examples in my own line of work:

- Laevo ([Jeuris et al., 2014][9]) presents an activity-centric software architecture integrating traditional task, window, and file management. As a systems research contribution, it envisions a future by prototyping a solution in which personal computer users are no longer burdened with file management. Instead, window configurations can be organized and persisted on a time line as part of task management.
- Socratrees ([Jeuris, 2018][10]) explores the design of a new information infrastructure to evaluate, contest, and reason about information online—as opposed to merely disseminating it. As a systems research contribution, it envisions a future in which claims represented in multiple media sources (e.g., this article) can link to a central repository of aggregated structured argumentation.

Considering systems research in this narrower sense, I find that the arguments presented below become all the more convincing and relevant.

## Decline in Systems Research

> In the early days of graphical user interfaces, the creation of new architectures for interactive systems was a lively and healthy area of research. [This has declined in recent years](http://socratrees.wiki/statement/details/1338). — [Olsen, 2007][2]

Olsen lists three reasons for this decline: (1) [stable and widely used platforms such as Windows, Mac, and Linux now dictate the user interface architecture](http://socratrees.wiki/statement/details/1347), (2) [current HCI researchers lack skills in toolkit or windowing system architecture and design](http://socratrees.wiki/statement/details/1349), and (3) [there is a lack of appropriate criteria for evaluating systems architectures](http://socratrees.wiki/statement/details/1355).

This last point specifically, a shortcoming in the review process, is what Olsen hopes to address in his paper. But, not much seems to have changed in the past 14 years, as this remains [a recurring limitation—and frustration—for HCI researchers that do have the necessary skill set to perform systems research and try to get it published](http://socratrees.wiki/statement/details/1357). Here are a select few excerpts in chronological order:

> [The reviewers simply do not value the difficulty of building real systems and how hard controlled studies are to run on real systems for real tasks.](http://socratrees.wiki/statement/details/970)  —   James Landay (**2009**). [I give up on CHI/UIST](https://dubfuture.blogspot.com/2009/11/i-give-up-on-chiuist.html)

> [[T]hose following a social science tradition ...  are often the most available reviewers for a systems paper on a social computing topic](http://socratrees.wiki/statement/details/1359) ... [and]...  [may reject a paper until it has conclusively proven an effect](http://socratrees.wiki/statement/details/1364) — Bernstein et al. (**2011**). [The trouble with social computing systems research][5]

> [E]ven with specific engineering committees at CHI and whole conferences such as EICS, there is still a lot of confusion about the science part, and [we still have a hard time acknowledging systems research](http://socratrees.wiki/statement/details/1369). ... [T]here is still little agreement among researchers on what makes good systems research. — Michael Nebeling (**2017**). [Playing the Tricky Game of Toolkits Research][7]

>  [R]esearchers experience toolkit papers as being hard to publish due to various biases ... [A]cceptance of toolkits as a research contribution remains a challenge and a topic of much recurrent discussion. — Ledo et al. (**2018**). [Evaluation Strategies for HCI Toolkit Research][6]

Simply put: [systems research is not valued as much as other types of contributions in HCI](http://socratrees.wiki/statement/details/1451).
As a result, this [gives academic researchers no incentive to do systems research](http://socratrees.wiki/statement/details/1007); it is a certain way to stall your academic career [as it is much harder to get system papers accepted than other types of contributions](http://socratrees.wiki/statement/details/1009). And, we all know that [publication count matters in academia](http://socratrees.wiki/statement/details/1011).

Arguably, [this is the main reason HCI systems research is in decline](http://socratrees.wiki/statement/details/1536); [why contribute your work to academia when greater incentives can be found elsewhere](http://socratrees.wiki/statement/details/1537), e.g., as commercial offerings or works of passion?

## Explosion of Empirical Research

Again, a parallel can be drawn with systems research outside of HCI. Many years ago, [Rob Pike (2000)][8] observed that operating systems research is a "field in decline".
Interestingly, many of the explanations and concerns he raised overlap.

> If systems research was relevant, we'd see new operating systems and new languages making inroads into the industry, the way we did in the '70s and '80s.
> Instead, we see a thriving software industry that largely ignores research, and a research community that writes papers rather than software.

> ... invention has been replaced by observation.

Could this be a recurring pattern?

I like to visualize HCI as an expanding field of research over time. As technology evolves, the context studied in user interface design expands ([Jeuris, 2017][11]; Figure 4).

> [O]riginally there was a focus on the hardware interface, followed by a focus on software, whereas most of HCI research today focuses on the work settings and its associated social context.

![As technology evolves, from hardware, to software, to desktop computing, to personal information management, to social media, the context studied in user interface design expands, and draws on different fields of research, from engineering, to mathematics, to programming, to design, to cognitive science, to social sciences.](/articles/assets/images/hci-context-expands.png)

Design research, cognitive science, and social sciences have contributed tremendously to our understanding on how to take into account a broader context when designing technologies, i.e., methods and theories to design better artifacts.

Simultaneously, observation studies have taught us the shortcomings and pitfalls of current systems.
Empirical research, from quantitative controlled experiments to qualitative ethnographies, are key components of the scientific method. As such, it's easy to see why they are readily accepted as research contributions in HCI.

However, shouldn't someone be incorporating these insights into new systems?
Unfortunately, each time a specific technology becomes mainstream, whether it is an operating system, window mangager, or social media platform, innovation in academia seems to stall, and is mostly reduced to running empirical studies on whatever system industry produces, or on small adaptations thereof.

## The End of Systems Research

[What once was the heart and soul of a growing new field](http://socratrees.wiki/statement/details/1456), and [gave rise to omnipresent technologies such as the Personal Computer](http://socratrees.wiki/statement/details/1491) and [World Wide Web](http://socratrees.wiki/statement/details/1493), is now a near-extinct line of research.
HCI shuns systematic generalizations and applauds creating evermore specific descriptions of practice and tools to support it.

Again, HCI is not alone in this. [Rob Pike (2000)][8] argues how this is the result of a "change of scale":

> [M]uch of the interesting work requires effort on a large scale. Many person-years are required to write a modern, realistic system. That is beyond the scope of most university departments.

> This means that industry tends to do the big, defining projects—operating systems, infrastructure, etc.—and small research groups must find smaller things to work on.

In other words: academic computer science research doesn't "go for breadth", it "go[es] for depth".

The few remaining researchers targeting _breadth_, i.e., systems research, are faced with the near-insurmountable task of convincing their "peers", inured in a _depth-first_ culture, that the work they do should be considered research at all. Complaints and examples abound on social media, e.g., [one reviewer's nonsensical claim that "this is a systems paper framed as a research paper"](https://twitter.com/joe_hellerstein/status/1064710469900890113).

I've observed the following paradox in systems research: **the bigger, more complex, system you are developing, the more research you draw on, the more likely reviewers will trivialize your contribution.**
In a way, this is understandable. Reviewers are asked to criticize your work, and systems research tends to raise many questions.
The more ground you cover, the more likely they'll be able to envision and spot missing features; the more related work you introduce, the more similarities they see, the more likely they'll see your work as "incremental" and argue the contribution is not large enough to warrant publication.

## Do We Need Systems Research?

Work in progress ...


## References

- Bernstein, M. S., Ackerman, M. S., Chi, E. H., & Miller, R. C. (2011). [The trouble with social computing systems research.][5] In CHI'11 Extended Abstracts on Human Factors in Computing Systems (pp. 389-398).
- Jeuris, S. (2017). [Task and Interruption Management in Activity-centric Computing][11] (Doctoral dissertation, IT University of Copenhagen, Software Development Group, Pervasive Interaction Technology Laboratory).
- Jeuris, S. (2018). [Socratrees: Exploring the Design of Argument Technology for Layman Users.][10] arXiv preprint arXiv:1812.04478.
- Jeuris, S., Houben, S., & Bardram, J. (2014). [Laevo: A temporal desktop interface for integrated knowledge work.][9] In Proceedings of the 27th annual ACM symposium on User interface software and technology (pp. 679-688).
- Ledo, D., Houben, S., Vermeulen, J., Marquardt, N., Oehlberg, L., & Greenberg, S. (2018, April). [Evaluation strategies for HCI toolkit research.][6] In Proceedings of the 2018 CHI Conference on Human Factors in Computing Systems (pp. 1-17).
- Levin, R., & Redell, D. D. (1983). [How (and how not) to write a good systems paper.][1] ACM SIGOPS Operating Systems Review, 17(3), 35-40.
- Nebeling, M. (2017). [Playing the Tricky Game of Toolkits Research.][7] In workshop on HCI. Tools at CHI.
- Olsen Jr, D. R. (2007). [Evaluating user interface systems research.][2] In Proceedings of the 20th annual ACM symposium on User interface software and technology (pp. 251-258).
- Pike, R. (2000). [Systems software research is irrelevant.][8] In Talk. CS Colloquium, Columbia University.
- Wobbrock, J. O., & Kientz, J. A. (2016). [Research contributions in human-computer interaction.][4] Interactions, 23(3), 38-44.

  [1]: https://www.usenix.org/legacy/event/samples/submit/advice.html
  [2]: https://dl.acm.org/doi/10.1145/1294211.1294256
  [3]: https://cacm.acm.org/blogs/blog-cacm/86066-what-makes-a-good-hci-systems-paper/fulltext
  [4]: http://faculty.washington.edu/wobbrock/pubs/interactions-16.pdf
  [5]: https://dspace.mit.edu/bitstream/handle/1721.1/64444/Miller_The%20Trouble.pdf%3Bjsessionid%3DD16AE455E533597043205F9490D9439B?sequence%3D1
  [6]: https://dl.acm.org/doi/abs/10.1145/3173574.3173610
  [7]: http://www.michael-nebeling.de/publications/chi17w.pdf
  [8]: http://doc.cat-v.org/bell_labs/utah2000/utah2000.html
  [9]: https://dl.acm.org/doi/10.1145/2642918.2647391
  [10]: https://arxiv.org/abs/1812.04478
  [11]: https://pure.itu.dk/ws/files/83014578/PhD_thesis_Final_Version._Steven_Jeuris_for_online.pdf
  