# Introduction to git

## Table of content

1. [Introduction](#introduction)
2. [Getting started](#getting-started)
    * [demo](#demo)
    * [First steps on embl git](#first-steps-on-embl-git)


**Contributors:** Nicolas Descostes and Toby Hodges

**Credits:** This content is largely based on the [GBCS](https://gbcs.embl.de/portal/tiki-index.php) [tutorial](https://gbservices.embl.de/git-conda/) and the [Software Carpentry](https://software-carpentry.org/) [tutorial](https://swcarpentry.github.io/git-novice/). 
The Software Carpentry content being under CC-BY 4.0 license and GBCS having kindly given their authorization to use their material, a lot of the material in this workshop are just copied/pasted.

 
## Introduction

**Slides:** [intro](pdf/intro.pdf)

Let's begin by having a look at what a life without git looks like:

![manuscript1](pictures/intro/intro1.jpeg)
[1](https://medium.com/@fredrick.adegoke/version-control-systems-source-code-banking-efcbb9272aee)

![manuscript2](pictures/intro/intro2.png)
[2](http://www.phdcomics.com)

Git can not only prevent you experiencing these situations but also help you programming more efficiently:

![badpractice](pictures/intro/intro3.jpeg)
[3](http://www.phdcomics.com)

Version control systems start with a base version of the document and then record changes you make each step of the way. You can think of it as a recording of your progress: you can rewind to start at the base document and play back each change you made, eventually arriving at your more recent version.

![modification1](pictures/intro/intro4.svg)

Once you think of changes as separate from the document itself, you can then think about “playing back” different sets of changes on the base document, ultimately resulting in different versions of that document. For example, two users can make independent sets of changes on the same document. Git enables collaborative work! Several people can work on the same document or the same program!

![modification2](pictures/intro/intro5.svg)

Unless multiple users make changes to the same section of the document - a conflict - you can incorporate two sets of changes into the same base document.

![modification3](pictures/intro/intro6.svg)

A version control system is a tool that keeps track of these changes for us, effectively creating different versions of our files. It allows us to decide which changes will be made to the next version (each record of these changes is called a commit), and keeps useful metadata about them. The complete history of commits for a particular project and their metadata make up a repository. Repositories can be kept in sync across different computers, facilitating collaboration among different people.

Automated version control systems are nothing new. Tools like RCS, CVS, or Subversion have been around since the early 1980s and are used by many large companies. However, many of these are now considered legacy systems (i.e., outdated) due to various limitations in their capabilities. More modern systems, such as Git and Mercurial, are distributed, meaning that they do not need a centralized server to host the repository. These modern systems also include powerful merging tools that make it possible for multiple authors to work on the same files concurrently.

**Key points:**
  * Version control is like an unlimited ‘undo’.
  * Version control also allows many people to work in parallel.

## Getting started

### Demo

**Live demo of the content of the next section.**

### First steps on embl git

1. Connect to **git.embl.de** and use your regular login and password.

![log](pictures/First-steps-on-embl-git/step1.png)


2. Explore the welcome page

![Welcome](pictures/First-steps-on-embl-git/step2.png)

  * A: By default, all the projects that you are involved in are displayed on this page. **A project is also called a 'repository'.**
  * B: When creating a project, you can define access rights (**private, internal, public**; see below). This tab will restrict the view to your projects that are **private**.
  * C: Search bar, search for a particular project by keywords.
  * D: Create a new project (see below).

  
3. Explore projects

![projects](pictures/First-steps-on-embl-git/step3.png)

  * A: Click on All to see all **repositories** hosted at EMBL. You can also filter these projects by 'Trending' or 'Most stars' features.
  * B: Display the repositories by 'last updated', 'name', 'oldest updated', and other criteria.
  * C: Display the repositories whether they are 'public', 'internal' or 'private'.
  * D: The 'New project' icon is always accessible from the interface (see next step).

  
4. Create a new project
  
![new project](pictures/First-steps-on-embl-git/step4.png)

  * A: Enter your project name such as 'Demo Repo'.
  * B: A repository slug is a URL-friendly version of a repository name, you can see that upper-case letters and space were removed ('demo-repo').
  * C: Enter a description of the repository such as 'first creation of a git repository'. This will be displayed under your repository name on the welcome page.
  * D: Choose the visibility level of the repository. 'private' means that only you and other owners (that you could invite) can see the repository; 'internal' means that only people from embl can see the repository; and 'public' makes the repository readable to anybody.
  * E: Initialize the repository with a markdown document called 'README.md'. Select this option. The description (see point C) and the title of your repository will appear in this document by default.
  * F: Click 'Create project'.

5. Explore the repository interface

![repository](pictures/First-steps-on-embl-git/step5.png)

  * A: Title of the repository. The lock icon indicates that the repository is private.
  * B: You will see later on what *commit* and *branches* means. Aside from the indicated size of the repository (depending on the files stored in it), you can add a license (defining the conditions of utilization of you documents and code) and some searchable tags.
  * C: The bell icon enables to define how you should be notified concerning modifications made to the repository. Star is functionning as 'likes' on twitter or facebook. The clone button is what you will use to import the repository on your computer or in a development interface. The fork button enables you to clone any (non-private) repository in order to modify it.
  * D: Indicate the branch on which you are (see below on how to create and use branches). The '+' icon enables to add new files or folders; you will almost never use this button. The history displays modifications made on your repository and the 'down arrow' icon is a download button.
  * E: This secton contains all the folders and files of your repository. For the moment there is only one file: 'README.md'. The 'Last commit' column displays the last modification message for each file. 'Last update' indicates when a particular modification happened.
  * F: The README file, it is usually used to create the documentation of your repository.  

6. Edit README.md

![readme modification](pictures/First-steps-on-embl-git/step6.png)

7. Modify and commit

![modify and commit](pictures/First-steps-on-embl-git/step7.png)

  * A: Indicate the edited file.
  * B: Modificaton of the document. Here the sentence is 'Doing my first modification'.
  * C:  


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~



## The GitLab Interface & First Steps

- log into git.embl.de
- show an example project
  - highlight key parts of project interface
  - show project history timeline
  - show blame for a single file
  - show how to view older versions of a file
- create a project from scratch
- add a README.md
- introduce basics of Markdown
- make a change to README via web interface
- commit and explain commit message
- repeat
- add new file(s)

## Working on the command line

- navigate to relevant directory
- clone repo && cd into project directory
- change global settings
  - `git config --global user.name`
  - `git config --global user.email`
  - `git config --global core.editor "nano -w"`
- mention `git init` - demo this at the end of day
- `git status`
- `git log`
- edit/create a file
- `git add`
- `git commit`
  - (if necessary) more about commit messages
  - imagine your future self as a collaborator, who won't know (remember) why you made the changes you're making
- make another change
- `git add`
- `git commit -m`
- mention `git commit -a` & warn about hazards of using it
- `git log`
  - `git log -N`
  - `git log --oneline`
  - `git log --patch <filename>`
- `git diff`
  - `git add + git diff --staged`
  - `git diff --color-words`
  - `git diff HEAD~2 <filename>`
  - `git diff <commithash> <filename>`
- `git checkout HEAD` to revert to most recent committed state
  - `git checkout HEAD <filename>` to achieve the same thing with a single file
- detached head!
  - `git checkout <commithash>` (forgetting filename)
  - `git checkout master` to recover from this
- `.gitignore`
- remotes
  - `git remote`
  - `git push origin master`
  - make a change on GitLab
  - `git pull origin master`
- collaboration exercises
 