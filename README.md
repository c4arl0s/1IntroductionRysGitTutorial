# [go back to Content](https://github.com/c4arl0s/RysGitTutorial#rys-git-tutorial)

# [1. Introduction - Content](https://github.com/c4arl0s/1IntroductionRysGitTutorial#go-back-to-content)

 * [A Brief History of Revision Control](https://github.com/c4arl0s/1IntroductionRysGitTutorial#-a-brief-history-of-revision-control)
 * [The birth of Git](https://github.com/c4arl0s/1IntroductionRysGitTutorial#-the-birth-of-git)
 * [Installation](https://github.com/c4arl0s/1IntroductionRysGitTutorial#-installation)
 * [Get Ready](https://github.com/c4arl0s/1IntroductionRysGitTutorial#-get-ready)

# [1. Introduction](https://github.com/c4arl0s/1IntroductionRysGitTutorial#1-introduction---content)

Git is a version control system (VCS) created for a single task: managing changes to your files. It lets you track every change a software project goes through, as well as where those changes came from. This makes Git an essential tool for managing large projects, but it can also open up a vast array of possibilities for your personal workflow.
 
# 	* [A Brief History of Revision Control](https://github.com/c4arl0s/1IntroductionRysGitTutorial#1-introduction---content)

We will talk more about the core philosophy behind Git in a moment, but first, let's step through the evolution of version control system in general.

# Files and Folders

Before the advent of revision control software, there were only files and folders. The only way to track revisions of a project was to copy the entire project and give it a new name. Just think about how many times you have saved a "backup" called my-term-paper-2.doc. This is the simplest form of version control.

![Screen Shot 2021-03-23 at 17 00 56](https://user-images.githubusercontent.com/24994818/112229864-5c80e200-8bf9-11eb-85e7-baa9111a430b.png)

But, it is easy to see how copying files from folder to folder could prove disastrous for software developers. What happens if you mis-label a folder?. Or if you overwrite the wrong file?. How would you even know that you lost an important piece of code?. It didn't take long for software developers to realize they needed something more reliable.

# Local VCS

So, developers began writing utility programs dedicated to managing file revisions. Instead of keeping old versions as independent files, these new VCSs store them in a database. When you needed to look at an old version, you used the VCS instead of accessing the file directly. That way, you would only have a single "Check-out" copy of the project at any given time, eliminating the possibility of mixing up or losing revisions.

![Screen Shot 2021-03-23 at 17 05 41](https://user-images.githubusercontent.com/24994818/112230154-0496ab00-8bfa-11eb-8cc6-f4cb011230b1.png)

At this point, versioning only took place on the developer's local computer - there was no way to efficiently share code amongst several programmers.

# Centralized VCS

Enter the centralize Version Control Systems. Instead of storing project history on the developer's hard disk, these new CVCS programs stored everything on a server. Developers checked out files and saved them back into the project over a network. This setup let several programmers collaborate on a project by giving them a single point of entry.

![Screen Shot 2021-03-23 at 17 09 08](https://user-images.githubusercontent.com/24994818/112230477-7f5fc600-8bfa-11eb-8d31-25d4299095a0.png)

While a big improvement on local VCS, centralized systems presented a new set of problems:

1. How do multiple users work on the same files at the same time ?.

Just imagine a scenario where two people fix the same bug and try to commit their updates to the central server. Whose changes should be accepted?.

CVCSs addressed this issue by preventing users from overriding other's work. If two changes conflicted, someone had to manually go in and merge differences. This solution worked for projects with relatively few updates (which meant relatively few conflicts), but proved cumbersome (incomodo) for projects with dozens of active contributors submitting several updates everyday: development could not continue until all merge conflicts were resolved and made available to the entire development team.

# Distributed VCS

The next generation of revision control programs shifted away from the idea of a single centralized repository, opting instead to give every developer their own local copy of the entire project. The resulting distributed network of repositories let each developer work in isolation, much like a local VCS - but now the conflict resolution problem of CVCS had a much more elegant solution.	
![Screen Shot 2021-03-23 at 17 18 29](https://user-images.githubusercontent.com/24994818/112231168-cdc19480-8bfb-11eb-94da-5c452cffb284.png)

Since there was no longer central repository, everyone could develop at their own pace, store the updates locally , and put off merging conflicts until their convenience. In addition, distributed version control systems (DVCS) focused on efficient management for separate branches of development, which made it much easier to share code, merge conflicts, and experiment with new ideas.

The local nature of DVCSs also made development much faster, since you no longer had to perform actions over a network. And, since each user had a complete copy of the project, the risk of a server crash, a corrupted repository, or any other type of data loss was much lower than that of their CVCS predecessors.

# 	* [The birth of Git](https://github.com/c4arl0s/1IntroductionRysGitTutorial#1-introduction---content)

And so, we arrive at Git, a distributed version control system created to manage the Linux Kernel. In 2005, the Linux community lost their free license to the BitKeeper software, a comercial DVCS that they had been using since 2002. In response, Linus Tolvalds advocated the development to a new open-source DVCS as a replacement. This was the birth of Git.

As a source code manager for the entire Linux Kernel, Git had several unique constraints, including:

1. Reliability.
2. Efficient management of large projects.
3. Support for distributed development.
4. Support for non-linear development.

While other DVCSs did exist at the time (example: GNU's Arch or David Roundy's Darcs), none of them could satisfy this combination of features. Driven by these goals, Git has been under active development for several years and now enjoys a great deal of stability, popularity, and community involvement.

Git originated as a command-line program, but a variety of visual interfaces have been released over the years. Graphical tools mask some of the complexity behind Git and often make it easier to visualize the state of the repository, but they still require a solid foundation in distributed version control. With this in mind, we will be sticking to the command-line interface, which is still the most common way to interact with Git.

# 	* [Installation](https://github.com/c4arl0s/1IntroductionRysGitTutorial#1-introduction---content)

The upcoming modules will explore Git's features by applying commands to real-world scenarios. But first, you will need a working Git installation to experiment with. Follow the instructions at [https://git-scm.com](https://git-scm.com).

To test you installation open a new command prompt and run:

Console output:

```console
$ git --version
```

Console output:

```console
git version 2.29.2
```

# 	* [Get Ready](https://github.com/c4arl0s/1IntroductionRysGitTutorial#1-introduction---content)
i
Remember that this tutorial is designed to demonstrate Git's feature set, not just give you a superficial overview of the most common commands. To get the most out of this tutorial, it is important to actually execute the commands you are reading about. So, make sure you are sitting in front of a computer, and let's get to it.

Awesome !!!
