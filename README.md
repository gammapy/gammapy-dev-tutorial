# Gammapy developer tutorial

## Introduction

This is the Gammapy developer tutorial for the [Gammapy coding sprint (Feb 2018, Paris)](https://github.com/gammapy/gammapy-meetings/tree/master/2018-02-05), given by [Christoph Deil](https://github.com/cdeil).

We have three half days (Tue, We, Thu morning), so six 1.5 hour sessions.

We aim to do something that's useful for most people. This is difficult given the mix of beginner (started coding recently, never made a code contribution to Gammapy) to expert (knows about Python, Numpy, Astropy, testing, documentation, the Gammapy codebase) at this meeting. The basic idea is that we will do a mix of beginner to intermediate lessons, and the experts can just work on their laptop in this room, or directly go to the other room.

## What you will learn

The goal is that you learn this:

1. How to work on Gammapy, have all the tools set up on your machine and know how to use them.
1. How to contribute to Gammapy via a pull request, i.e. know how to use git and Github and how the code review process works

For a more detailed overview, please see the agenda below.

We will focus on the "craft" aspect of working on Gammapy, leaving the "art" aspect to the rest of the week. What I mean by "craft" is that you will learn how to use the tools (git, Github, Python, Jupyter, pytest, Sphinx, PyCharm) efficiently. And what I mean by "art" is that to make a contribution you will still need to figure out what algorithms and interface to implement, i.e. what to do. For that, we have the rest of the week, and the coming weeks, months, years. But everyone struggles with git and pytest and Sphinx the first time they use it, and it's good to have that out of the way for when the time comes for your first "real" pull request to Gammapy, that fixes some issue or adds new functionality.

The tutorials will be very hands-on. Mostly demos you can follow along, and exercises, I have no slides. We are flexible, i.e. the level and content will be adjusted bases on your suggestions as we go. Please speak up and ask any questions and suggest what to cover any time!

## Prepare

Here's how you can prepare for the tutorials. If you have any questions or issues, please contact me (Christoph) on Gammapy Slack or via email (listed at [Christoph Deil](https://github.com/cdeil)).

* Join the Gammapy mailing list and Gammapy Slack (see http://gammapy.org/contact.html). Email me if you want to be added to the Slack.
* Make a Github account (it's free). Install git if you don't have it already. Set up SSH keys or your key chain so that you don't have to type your username and password all the time. Infos are at https://help.github.com/ .
* If you've never used git, please do this 15 min tutorial (https://try.github.io)
* If you've never used Github, please do the "Understanding the Github flow" and "Hello world" tutorials at https://guides.github.com/ (should take 15 - 30 min)
* Install Python 3 with Numpy, Scipy, Astropy, pytest, sphinx, and git clone gammapy. If you don't have that set up already we recommend you get Python 3.6 from Anaconda, and the create the `gammapy-dev` conda environment as described [here](http://docs.gammapy.org/dev/development/intro.html#get-set-up).
* If you like, you could install and try out [JupyterLab](http://jupyterlab-tutorial.readthedocs.io/) instead of the classic Jupyter notebook. It's still alpha software, but I've been using it for the past few months and it's been working well and I like it better than the classic Jupyter notebook interface. You can go back and forth any time, the Jupyter notebook file format is the same, it's just a different web interface.
* If you're new to Python, scientific Python or Astropy, here are some good tutorial resources to get you started: http://docs.gammapy.org/dev/tutorials.html#the-basics . Really all we need for the tutorials is that you have a little experience writing Python code, like what's covered [here](http://nbviewer.jupyter.org/github/jakevdp/WhirlwindTourOfPython/blob/master/Index.ipynb). We will probably use some Numpy, Astropy and Gammapy functionality in examples, but it will not be a focus.
* Install a code editor or IDE. For the past few years, I've used [PyCharm](https://www.jetbrains.com/pycharm/) and I think it's great, I recommend you give it a try for this week and see if you like it. At least you'll see me demo / use it in the tutorials. The commmunity edition is open source and free and easy to install on Mac, Linux and Windows. The professional version mainly has extra stuff for web development that we don't need. It takes a few minutes to get set up, I will show you how to do it in the tutorial, no need to do anything before except to install it. If you don't want to try out PyCharm, other common good code editor options are the old-school vim or emacs, or the modern [Atom](https://atom.io/) (from Github team) or [Visual Studio Code](https://code.visualstudio.com/) (from Microsoft team). All of those four are cross-platform and open source, they are not commercial products.
* We will mostly teach git concepts and how to use it from the command line and Github web interface, and a little bit from PyCharm. You can also do git from your editor / IDE, all of the ones just mentioned support this directly or after installing a plugin. This can be quicker / simpler / nicer than the command line. Some people use extra [Git GUI apps](https://git-scm.com/downloads/guis) like [Github Desktop](https://desktop.github.com/). I'm not using those, so I won't cover them / you don't need to install them. I just wanted to mention the option.

That said, if you arrive at the tutorial without having anything installed or knowing anything, you are of course still welcome, and we'll just help you get set up and started there.

## Resources

Many of you will not use the tools and commands we learn here regularly, and will forget them. We hope that you will remember the concepts and key terms (like git commit, branch, pull, push, merge, rebase, ...). If so, usually a Google search for what you want to do will yield a StackOverflow question and answer for what you need.

In addition, we will distribute printouts of the following "cheat sheets" at the beginning of the tutorials that can be helpful to remember how to do things, or to take extra notes:
* [conda](https://conda.io/docs/_downloads/conda-cheatsheet.pdf)
* [Git](https://services.github.com/on-demand/downloads/github-git-cheat-sheet.pdf)
* [Pycharm Mac](https://resources.jetbrains.com/storage/products/pycharm/docs/PyCharm_ReferenceCard_mac.pdf), [Pycharm Linux/Windows](https://resources.jetbrains.com/storage/products/pycharm/docs/PyCharm_ReferenceCard.pdf)

Other webpages with tutorials and documentation that you might find useful to learn or as a reference:
* Python references (not sure how useful those are): [one](https://learnxinyminutes.com/docs/python3/), [two](http://nbviewer.jupyter.org/github/justmarkham/python-reference/blob/master/reference.ipynb), [three](https://nbviewer.jupyter.org/github/oreillymedia/python_epiphanies/blob/master/Python-Epiphanies-All.ipynb)
* pytest: https://docs.pytest.org, https://github.com/jiffyclub/pytest-features
* sphinx: http://www.sphinx-doc.org/, https://github.com/cdeil/sphinx-tutorial
* PyCharm: https://www.jetbrains.com/help/pycharm/
* git: https://git-scm.com/
* Github: https://help.github.com/

The Gammmapy developer documentation is very much work in progress.
However, for Astropy there is a lot written up, and almost everything applies 1:1 in Gammapy.

* Gammapy developer documentation: http://docs.gammapy.org/dev/development/
* Astropy developer documentation: http://docs.astropy.org/en/latest/#developer-documentation

## Lessons

### Tuesday 9:00 - 10:30

* Executing Python code (Python, ipython, Jupyter); understand imports, modules, def, class, ...
* Installing Python packages (setuptools, pip, conda); understand sys.path and sys.modules

### Tuesday 11:00 - 12:30

* Writing Python code (with an editor like emacs/Atom/Visual Studio Code or an IDE like PyCharm)
* Debugging Python code (print, with IPython, with PyCharm)
* Reading / navigating a large codebase (Gammapy, using PyCharm)

### Wednesday 9:00 - 10:30

* Writing automated tests (with pytest)
* Writing documentation (with ReStructuredText and Sphinx)

### Wednesday 11:00 - 12:30

* Learn git and Github
* Code review from the contributor and reviewer perspective

### Thursday 9:00 - 10:30

* A big exercise for the whole workflow, to be done in pairs. Team up with your neighbor now!
* Using this repo (https://github.com/cdeil/gammapy-dev-tutorial), in the `practice` folder, do all the steps to make a code contribution. Start by making a new git branch. Make a sub-folder with your github username. Write some code (a small function or class, whatever you like, 3 lines of code are OK. Write a test and use pytest to run it. Write a docstring in the Numpy docstring format. Make a pull request against my repo. Go through one round of code review to practice Github / git. Goal: have it merged before the coffee break (10:30).
* Who has done this before? If this is too easy for you, then just do something else! E.g. you could practice git and collaborate on the branch from two machine, introduce merge conflicts, do a rebase. Or practice Python coding or pytest, and develop some code and tests together; discuss patterns to structure code and tests. Or show each other how you do Python coding / debugging. 

### Thursday 11:00 - 12:30

* Open space. Practice. Ask any question. Get help.
