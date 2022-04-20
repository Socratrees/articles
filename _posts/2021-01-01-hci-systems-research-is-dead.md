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
Systems research seeks _systematic_ solutions to a broad set of problems by cohesively incorporating a large body of prior work.
In this broader context, one could thus view HCI systems as **user interfaces that connect applications together**.

It is [the interplay between software architecture and the novel cross-application user interactions it enables](http://socratrees.wiki/statement/details/1531) which, to me, sets HCI systems research apart from mere "applications".
Often, systems research tries to _reimagine_ what an "application" is. Two examples in my own line of work:

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

Again, a parallel can be drawn with systems research outside of HCI. Many years ago, [Rob Pike (2000)][8] observed that [operating systems research is a "field in decline"](http://socratrees.wiki/statement/details/1543).
Interestingly, many of the explanations and concerns he raised overlap.

> If systems research was relevant, we'd see new operating systems and new languages making inroads into the industry, the way we did in the '70s and '80s.
> Instead, we see a thriving software industry [that largely ignores research](http://socratrees.wiki/statement/details/1539), and a research community [that writes papers rather than software](http://socratrees.wiki/statement/details/1540).

> ... [invention has been replaced by observation](http://socratrees.wiki/statement/details/1541).

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

> We predominantly produce technology that is somewhat better than its antecedents, but these technologies rarely make it into the commercial world (although they may influence it somewhat). We also see technologies that are highly successful but not developed by the CHI community, so we are left to evaluate its usability only after the fact. — [Greenberg & Buxton, 2008][12].

Again, HCI is not alone in this. [Rob Pike (2000)][8] argues how this is the result of a "change of scale":

> [M]uch of the interesting work requires effort on a large scale. Many person-years are required to write a modern, realistic system. That is beyond the scope of most university departments.

> This means that industry tends to do the big, defining projects—operating systems, infrastructure, etc.—and small research groups must find smaller things to work on.

In other words: academic computer science research doesn't "go for breadth", it "go[es] for depth".

The few remaining researchers targeting _breadth_, i.e., systems research, are faced with the near-insurmountable task of convincing their "peers", inured in a _depth-first_ culture, that the work they do should be considered research at all. Complaints and examples abound on social media, e.g., [one reviewer's nonsensical claim that "this is a systems paper framed as a research paper"](https://twitter.com/joe_hellerstein/status/1064710469900890113).

This is only human: reviewers are asked to criticize your work, and systems research tends to raise many questions.
The more ground you cover, the more likely reviewers will be able to envision and spot missing features. The more related work you introduce, the more similarities with other systems they'll see.
The latter, more often than not, leads to contributions being labeled as "incremental", which out of hand is equated with "too small to warrant publication"; so much for ["standing on the shoulders of giants"](https://en.wikipedia.org/wiki/Standing_on_the_shoulders_of_giants).
And due to the large scope covered by systems research, even the most constructive reviews will request details you may have omitted intentionally to make space for information requested as part of a previous reviewing round.
This leads to the following paradox in systems research: **the bigger, more complex, system you are developing, the more research you draw on, the more likely reviewers will trivialize your contribution and request additional work to be done.**

Not only does this make it hard to publish systems research, it incentivizes _bad_ research:

- When confronted with a design challenge, don't look for a solution beyond the specific context in which it was first observed or you obtained funding for. The _external validity_ of your work is less important than presenting novel and positive findings. The more you scope your work, the easier it is to argue for novelty and the less variance in the data you collect.
- Limit the introduction of related systems of fields that your "peers" are unlikely to know about, and abstain from highlighting how your work is similar. It will unncessarily decrease your chances of getting accepted.
- Don't report on design challenges you uncover as part of creating and using an "interactive sketch" ([Greenberg & Buxton, 2008][12]). Many reviewers will treat such design insights as a failed empirical evaluation and ask you to revise and resubmit.

But don't take my word for it. Here are some reviews, exemplary of the points made above, of past submissions of mine.
Their sole purpose is to demonstrate where frustrations of systems researchers with the review process come from, so if you are familiar with this firsthand, feel free to [skip to the next section](#do-we-need-systems-research). 

### Examples of system paper reviews: Laevo

My very first submission, a [works-in-progress paper to CHI 2013]({{ site.baseurl }}{% link /assets/files/CHI2013-Laevo-submission.pdf %}), presented a window manager which "repurpose[s] the calendar metaphor to not only plan tasks, but also to provide an overview of ongoing tasks, allow switching between them, and reflecting on past tasks." But, this was not deemed novel enough since previous window managers also included temporal features, and though some novelty was recognized, the work was deemed too preliminary for a _works-in-progress_ submission (meta rating 2/5). The paper was based on my MSc thesis, representing half a year worth of work, and presented the design rational and initial evaluation of a fully-functioning system.

> I have concerns about the novelty of the work. The author's core idea of providing a temporal way to organize groups of windows has been done before.
... Again, the author's ideas are good ones, but unfortunately it seems like they are not novel enough to the CHI community at this stage. Still, let me emphasize there are some very cool, novel aspects of the author's work which are not thoroughly explored--such as integration of the user's window/task manager with their calendar.
... And while I don't think there is enough novelty in this submission to make it a good fit for WiP, I look forward to seeing how this work evolves in the future. — **rated 2/5 by "Expert"**

> But, if one thinks of a window as simply a very large icon, then Timescape [cited related work] seems awfully similar to the system presented in this submission. — **rated 2/5 by "Knowledgeable"**

A full paper incorporating an additional year of work, including additional features uncovered as part of the previous evaluation and a new two-week in-situ field study, [was submitted to CHI 2014]({{ site.baseurl }}{% link /assets/files/CHI2014-Laevo-submission.pdf %}) and "was discussed in detail at the PC and the decision was not to accept the paper due to the incremental nature of the contribution" (meta rating 3/5).

> The system itself has similarities with those described in the literature review both in terms of its features and presentation. It is therefore more a variation on a theme rather than something notably original. — **rated 3.5/5 by "Knowledgeable"**

> It would be interesting to see what results you would garner if a longer field study such as three months would reveal about the use of your application.
... Various tools have been implemented to help support a timeline of tasks notably Trello which is web based and collaborative. According to Wikipedia Trello has over 1 million users. — **rated 3/5 by "Passing Knowledge"**

A slightly polished resubmission to UIST 2014 got lucky and got in ([Jeuris et al., 2014][9]), but still only had a meta rating of 3/5. Even the most positive reviewers struggle to understand the nature of systems research as a cohesive _broad_ contribution, as opposed to an _in depth_ measurable contribution towards one specific topic. They _see_ the contribution, but simply don't consider it large or strong enough to warrant publication. They "look forward to seeing this work in the future", but don't realize that without getting intermittent work published, there is no future for academic work like this.

> Unfortunately, all reviewers struggled to understand the extent to which there was a research contribution.
... I worry, however, that these contributions were spread thin among all areas, making it difficult to understand where the true meat is. — **Meta Review**

> I understand the struggle of a systems paper that you face: you've combined a lot of design descisions that are working together, and it is difficult to ply them apart to study one in depth in the absence of the others.
... I appreciate the value of demonstrating a concept, and I think the concept you are working on is worth pursuing, but I do not think the particular qualitative analysis you performed was strong enough to draw *conclusions* about that concept. — **rated 3/5 by "Knowledgeable"**

> I would consider the current state of Laevo as a concept under development. — **rated 3/5 by "Expert"**

As anticipated in the discussion section of Laevo, introducing support for collaboration was the next logical step.
A submission to CSCW 2016 did exactly that and presented co-Laevo ([archived as a technical report][13] after it was rejected with meta rating 2/5).
Taking heed of the previous reviewers' warning not to spread contributions too thin, this paper focused on design and implementation only.
Arguably this was too small of a contribution for a high-impact conference such as CSCW, but this was not the main point reviewers were complaining about.

> The paper states that its approach is different from other ABC systems but what about non-ABC systems?
... The paper presents no study which compares this system to current systems. — **rated 2/5 by "Passing Knowledge"**

One reviewer even believed Laevo already supported coordination and collaboration based on their reading of our research group's overarching project descriptions, rather than the cited UIST paper. But the same reviewer also referred to "the Laevo company web page". This may just be your average loose cannon you get in reviews from time to time, but they clearly still shaped the meta reviewer's opinion.

> Well, visiting http://pitlab.itu.dk/research, it is somehow hard to believe that Leavo does not address "coordination and collaboration within cooperating teams".
After all, that web page shows global interaction, http://pitlab.itu.dk/research/global-interaction, and pervasive healthcare, http://pitlab.itu.dk/pervasive-healthcare. — **rated 2/5 by "Knowledgeable"**

> All reviewers could not see the novel contribution of this paper in compare [sic] to the previous version of the system or to other existing systems. — **Meta Review**


## Do We Need Systems Research?

Work in progress ...


## References

- Bernstein, M. S., Ackerman, M. S., Chi, E. H., & Miller, R. C. (2011). [The trouble with social computing systems research.][5] In CHI'11 Extended Abstracts on Human Factors in Computing Systems (pp. 389-398).
- Greenberg, S., & Buxton, B. (2008). [Usability evaluation considered harmful (some of the time).][12] In Proceedings of the SIGCHI conference on Human factors in computing systems (pp. 111-120).
- Jeuris, S., Tell, P., Bardram, J. (2016) [co-Laevo: Supporting Cooperating Teams by Working ‘within’ Shared Activity Time Lines][13] Technical Report at IT University of Copenhagen (TR-2016-193).
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
  [12]: https://dl.acm.org/doi/abs/10.1145/1357054.1357074
  [13]: https://pure.itu.dk/portal/en/publications/colaevo--supporting-cooperating-teams-by-working-within-shared-activity-time-lines(ad1f6194-1116-4217-9adc-3ce21df3829f).html
