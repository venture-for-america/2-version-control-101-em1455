# Introduction to Version Control

> "The past is never where you think you left it." &mdash; [Katherine Anne Porter][KAP]

## Problem Statement

Have you created a document that you simply did not want to mess up? Maybe it
was a team project or a thesis?

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">Finally, a chance to edit my paper! Let&#39;s open the folder.<br><br>draft<br>draftFinal<br>draftUpdateFinal<br>draftUpdateFinalFinal<br>draftUpdateFinalFinal2<br>draftUpdateFinalNew<br>finalDraftFinal<br>finalDraftFinalRevised<br>finalDraftFinalUpdate<br>newDraft<br>newDraft2<br>newDraftUpdate<br>revisedDraftFinal<br><br>Umm...</p>&mdash; Lego Grad Student (@legogradstudent) <a href="https://twitter.com/legogradstudent/status/979527370066579456?ref_src=twsrc%5Etfw">March 30, 2018</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

There's gotta be a better way! Thankfully there is!

## Objectives

1. Identify the purpose of Version Control Systems (VCS)
2. Compare and contrast VCS and tracked changes in files
3. List other features of `git` at a high-level


## Identify The Purpose Of Version Control Systems (VCS)

The version control strategy shown in the tweet is not a bad one! We'll call
that "filename version control." Most often filename version control relies on
naming the versions in a way that captures:

* The reason a new version was made, its _motivation_
* The _time_ the new version was made

But recording this in the file name is error-prone and, well, ugly. It also
requires constant fiddling to update to the right file. We'd probably rather
get a new version of `index.html` and hit refresh versus getting
`index-20180619T0815.html` and navigating to it.

Software that allows us to create multiple versions of the same file and to log
_metadata_ ("data about the data") about the file (time created, intention behind
the change) is called a Version Control System (VCS).

We will learn the [`git`][git-getstarted] VCS. Other VCS systems are Mercurial
(program-name: `hg`), Subversion (program-name: `svn`), and CVS (program-name:
`cvs`).

## Compare and Contrast VCS And Tracked Changes In Files

You might be familiar with the idea of _version control_ for a document from
the "History" feature of Google Docs or "Track Changes" of Microsoft Word.
These are similar to `git` and other VCS, but the VCS programs offer some real
advantages.

Google Docs' and Word's snapshots don't allow us to record _motivation_.
They're also limited because they're the history of only _one_ file. Version
Control Systems (VCS) allow us to create, review, and share snapshots of whole
_projects_.

A VCS can record in one place:

* What files changed _and how_, the **version**:
  * Edited `index.html`: change `<img>` tag `src` from `coming_soon.jpg` to
    `byron_the_poodle.jpg`
  * Added new file `project-poodle.html`
  * Added new file `project-poodle.css`
  * Deleted `project-poodle-coming-soon.html`
* What **time** that change was recorded
* What the **motivation** behind the change was: "Launch project Poodle, an app to
  spread the joy and love of poodle-ownership via the web!"

Not only does `git` provide basic version control, it has many other features.

## List Other Features Of `git` At a High-level

While `git` allows you to record versions of your projects, that's just the tip
of the iceberg. We'll cover some of its most important features at a very high
level. The point here isn't to necessarily understand the mechanics and
commands, but to appreciate the work that `git` helps make easy. Because it
makes saving work, recovering, experimenting with ideas, and integrating
feedback so easy, it's no wonder `git` is regularly listed as a required skill
for jobs.

### Branching

Most people have reached a point in life where they had a choice: to do
something risky or to do something safe but slower.

![A Choice in "Oregon Trail" to ford the river](https://curriculum-content.s3.amazonaws.com/web-development/git-version-control-101/choices.gif "You tried to ford the river, didn't you?")

Given the choice, they have said "YOLO, do the risky thing!"

![A Bad Fording](https://curriculum-content.s3.amazonaws.com/web-development/git-version-control-101/11-21-10-bad-river-cross.gif "Regret")

...and regretted it.

Life, sadly, has no undo button.  Wouldn't it be great if you could try things
out in "sandbox" and then throw it away, with no consequence, if it didn't work
out? "Branches" in `git` allow exactly this. You can propose "parallel
universes" of code that can be compared, discussed, tried out, and ultimately
imported or thrown away.

### Tracking "`diffs`"

Earlier we said that `git` can track what changed between versions. It doesn't
do this with English text. Instead it uses a shorthand called a `diff`, short
for "difference".

![A diff on GitHub](https://curriculum-content.s3.amazonaws.com/web-development/git-version-control-101/diff_sample.png)

_This document is managed in `git`!_

Even after a revision is made, `git` users can find out which version made the
change (addition, deletion, edit), who created it, and _why_. This speeds
communication and allows worldwide collaboration because developers can
communicate their intentions _with their changes_.

### Sharing History / GitHub

By design, `git` was designed to help developers collaborate and propose
"diffs" to existing code. In fact, the first project to use `git` was,
arguably, the most successful open source product ever, Linux. Once the
benefits of `git` were discovered in that project, GitHub launched as a social
network for `git` authors. It is now the most popular code host in the world.
Understanding `git` will allow you to learn from others' code, collaborate to
create new things, and to show off your creations.

## Conclusion

In this lesson we've covered the basics of VCS systems and how they differ from
"filename version control." We've explained that VCS systems record metadata
about their versions. Given its popularity, we've chosen to introduce `git` and
some of its high level features. In subsequent lessons, we'll dive deeper into
`git`.
## Resources

* [Getting Started - About Version Control](http://git-scm.com/book/en/Getting-Started-About-Version-Control)
* [Git Basics - What is Git?][git-getstarted]

<p data-visibility='hidden'>View <a href='https://learn.co/lessons/git-version-control-101' title='Intro to Version Control'>Intro to Version Control</a> on Learn.co and start learning to code for free.</p>



[KAP]: http://en.wikipedia.org/wiki/Katherine_Anne_Porter
[git-getstarted]: http://git-scm.com/video/what-is-git
