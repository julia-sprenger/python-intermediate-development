---
title: Setting the Scene
start: no
colour: '#FBED65'
teaching: 15
exercises: 0
---

::::::::::::::::::::::::::::::::::::::: objectives

- Setting the scene and expectations
- Making sure everyone has all the necessary software installed

::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::: questions

- What are we teaching in this course?
- What motivated the selection of topics covered in the course?

::::::::::::::::::::::::::::::::::::::::::::::::::

## Introduction

So, you have gained basic software development skills either by self-learning or attending,
e.g., a [novice Software Carpentry course][swc-lessons].
You have been applying those skills for a while by writing code to help with your work
and you feel comfortable developing code and troubleshooting problems.
However, you are working on a shared project with some colleagues and need 
to organize the development across contributors and machines.

This course provides the next steps in how to setup and work collaboratively 
on a data project at the OECD.

This course requires basic knowledge in Python, Git, Shell and the access to the OECD Algobank. For introductions on those topics, see the OECD-customized [Python](https://julia-sprenger.github.io/python-novice-gapminder/), [Unix Shell](https://julia-sprenger.github.io/shell-novice/) and [Git](https://julia-sprenger.github.io/git-novice/) courses.


<!-- The course is organised into the following sections:

![Course overview diagram](fig/course-overview.svg){alt="Course overview diagram. Arrows connect the following boxed text in order: 1) Setting up software environment 2) Verifying software correctness 3) Software development as a process 4) Collaborative development for reuse 5) Managing software over its lifetime."} -->

<!---
Source of the above image can be rendered in the Mermaid live editor:
<https://mermaid.live/edit#pako:eNpdkE1rwzAMhv-K8CmFNrCvSw6D9eO2XlbYYeSiJXJqcKwgKyml9L_PaZox5pOQn8ey3oupuCZTGOv5VB1RFN4_ygDpvGUPORxI1YUG-m5qRrZ6QiGgMDjh0FLQBZRhtXqFdfaYwyeJs-ek_OMrFqFKA8U485vsKQ2YgZoG8tyND8LkYgSETrganUnZZs85bNh7_GZBdQPd2b-2ZQGhPtJd2mUvOewxYDNu8vujSeSBBJxG8M6SupYWZmlakhZdnWK5jFRp9EgtlaZIZU0We6-lKcM1odgrH86hMoVKT0vTdzUqbR02gq0pLPqYulQ7ZdlPUd8Sn8nd7Wa2OwxfzLN3_QE4H4oo>

The mermaid source is (with one less dash in arrows than needed):

```mermaid
flowchart LR
  A(1. Setting up software environment) -> B(2. Verifying software correctness)
  B -> C(3. Software development as a process)
  C -> D(4. Collaborative development for reuse)
  D -> E(5. Managing software over its lifetime)
```
-->

### [Section 0: Setting up the Data Project]

- Create a new project folder `myproject` in the `V:` drive.
- Open the `V:\myproject` folder in VSCode.
- Check that Python as well as git are available locally by executing `python` and `git` in the terminal. If this raises an error as those are not installed go to the workshop setup instructions for more details on how to install them.
- Initialize the git repository `git init`
- Login to the Algobank and create a corresponding new empty project.
- Setup the link between the local and remote (Algobank) project `git remote add https://gitlab.algobank.oecd.org/<GROUP>/<PROJECT_NAME>`.


We will start with template structure of an OECD Data project containing the following empty folders:

- `sources` for storing the source data files
- `sandbox` for temporary files
- `results` for analysis results
- `documentation` for supplementory documentation files
- `dissemination` for results to be uploaded in the Dot Stat Suite and to be displayed in the OECD Data Explorer
- `archive` for outdated / cold files
- `links` is populated with tools requested for the project, see the full list of tools which can be requested in the `P:` drive


In the project folder create those empty folders accordingly

```bash
mkdir -p V:/myproject/{sources,sandbox,results,documentation,dissemination,archive,links}
```

### [Section 1: Setting up Software Environment](10-section1-intro.md)

In the first section we are going to set up our working environment
and familiarise ourselves with various tools and techniques for
software development in a typical collaborative code development cycle:

- **Virtual environments** for **isolating a project** from other projects developed on the same machine
- **Command line** for running code and interacting with the **command line tool Git** for
- **Integrated Development Environment** for **code development, testing and debugging**,
  **Version control** and using code branches to develop new features in parallel,
- **Algobank** (or any other central and remote source code management platform supporting version control with Git)
  for **code backup, sharing and collaborative development**, and
- **Python code style guidelines** to make sure our code is
  **documented, readable and consistently formatted**.

### [Section 2: Verifying Software Correctness at Scale](20-section2-intro.md)

Once we know our way around different code development tools, techniques and conventions,
in this section we learn:

- how to set up a **test framework** and write tests to verify the behaviour of our code is correct, and
- how to automate and scale testing with **Continuous Integration (CI)** using
  **GitLab Actions** (a CI service available on the Algobank).

### [Section 3: Software Development as a Process](30-section3-intro.md)

In this section, we step away from writing code for a bit
to look at software from a higher level as a process of development and its components:

- different types of **software requirements** and **designing and architecting software** to meet them,
  how these fit within the larger **software development process**
  and what we should consider when **testing** against particular types of requirements.
- different **programming and software design paradigms**,
  each representing a slightly different way of thinking about,
  structuring
  and **implementing** the code.

### [Section 4: Collaborative Software Development for Reuse](40-section4-intro.md)

Advancing from developing code as an individual,
in this section you will start working with your fellow learners
on a group project (as you would do when collaborating on a software project in a team), and learn:

- how **code review** can help improve team software contributions,
  identify wider codebase issues, and increase codebase knowledge across a team.
- what we can do to prepare our software for further development and reuse,
  by adopting best practices in
  **documenting**,
  **licencing**,
  **tracking issues**,
  **supporting** your software,
  and **packaging software** for release to others.

### [Section 5: Managing and Improving Software Over Its Lifetime](50-section5-intro.md)

Finally, we move beyond just software development to managing a collaborative software project and will look into:

- internal **planning and prioritising tasks** for future development
  using agile techniques and effort estimation,
  management of **internal and external communication**,
  and **software improvement** through feedback.
- how to adopt a critical mindset not just towards our own software project
  but also to **assess other people's software to ensure it is suitable** for us to reuse,
  identify areas for improvement,
  and how to use GitHub to register good quality issues with a particular code repository.

## Before We Start

A few notes before we start.

:::::::::::::::::::::::::::::::::::::::::  callout

## Prerequisite Knowledge

This is an intermediate-level software development course
intended for people who have already been developing code in Python (or other languages)
and applying it to their own problems after gaining basic software development skills.
So, it is expected for you to have some prerequisite knowledge on the topics covered,
as outlined at the [beginning of the lesson](../index.md#prerequisites).
Check out this [quiz](../learners/quiz.md) to help you test your prior knowledge
and determine if this course is for you.


::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::::  callout

## Setup, Common Issues \& Fixes

Have you [setup and installed](../learners/setup.md) all the tools and accounts required for this course?
Check the list of [common issues, fixes \& tips](../learners/common-issues.md)
if you experience any problems running any of the tools you installed -
your issue may be solved there.


::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::::  callout

## Compulsory and Optional Exercises

Exercises are a crucial part of this course and the narrative.
They are used to reinforce the points taught
and give you an opportunity to practice things on your own.
Please do not be tempted to skip exercises
as that will get your local software project out of sync with the course and break the narrative.
Exercises that are clearly marked as "optional" can be skipped without breaking things
but we advise you to go through them too, if time allows.
All exercises contain solutions but, wherever possible, try and work out a solution on your own.


::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::::::  callout

## Outdated Screenshots

Throughout this lesson we will make use and show content
from Graphical User Interface (GUI) tools such as Visual Studio Code and the Algobank
These are evolving tools and platforms, always adding new features and new visual elements.
Screenshots in the lesson may then become out-of-sync,
refer to or show content that no longer exists or is different to what you see on your machine.
If during the lesson you find screenshots that no longer match what you see
or have a big discrepancy with what you see,
please [open an issue]({{ site.github.repository_url }}/issues/new) describing what you see
and how it differs from the lesson content.
Feel free to add as many screenshots as necessary to clarify the issue.


::::::::::::::::::::::::::::::::::::::::::::::::::



:::::::::::::::::::::::::::::::::::::::: keypoints

- This lesson focuses on core, intermediate skills covering the whole software development life-cycle that will be of most use to anyone working collaboratively on code.
- For code development in teams - you need more than just the right tools and languages. You need a strategy (best practices) for how you'll use these tools as a team.
- The lesson follows on from the novice Software Carpentry lesson, but this is not a prerequisite for attending as long as you have some basic Python, command line and Git skills and you have been using them for a while to write code to help with your work.

::::::::::::::::::::::::::::::::::::::::::::::::::

[swc-lessons]: https://software-carpentry.org/lessons/
