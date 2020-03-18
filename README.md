![code review image](https://www.bounteous.com/sites/default/files/styles/default/public/insights/2019-06/previews/20190606_blog_code_review_limbo-_how_low_should_you_go_website.png?itok=9Ly27cK0) 

# Code review with git & R
This is a repository for an internal [SoBA lab](https://www.soba-lab.com/) tutorial on how to do code review with git with some slides and a little R-script to practice code review. On top of our own crash course, we are also showcasing some resources that we have found useful in learning how to use git with R. If in this short introduction you get confused about terms, refer to the glossary below! :bowtie:  

For this introduction to code review with git and R, we are making a few assumptions.  
* You use R/ R projects in your scientific practice.
* You have heard of Github & using Github for version control.
* You want to learn a brand new way of thinking about version control, code review and want to throw yourself into this adventure with reckless abandon. 

## Why should you do code review?
It is helpful to think of code review as being one small part in "transitioning your workflow". I first started thinking about this when I heard the talk of the same name by Danielle Navarro at the Research Bazaar Sydney in 2019: https://slides.com/djnavarro/workflow#/  

Danielle is a computational cognitive scientist at the University of New South Wales (UNSW). In her talk, she argues that to help future you, you can make some small changes in your scientific workflow. By using tools such as R (for data analysis), OSF (for pre-registration and data sharing), git/ Github (for version contorl & code review) and PsyArXiv (for sharing pre-prints), we can improve the overall quality of our science.  

Lindsay Peterson (also based at UNSW) argues that code review can enhance research training, collaboration, and communication (slides shared in repo, with permission). She says it enhances student involvement, while the supervisor still has oversight. It helps with learning how to code, and students gradually move from reviewing to authoring code as their skills improve. She also points out that this practice helps with producing readable code, as you are writing with your reviewer/ collaborator in mind.  

Finally we get also: **BETTER, LESS BUGGY CODE**

## Intro to git - the unloved sibling of code review
According to Danielle "learning git is one of the hardest steps. We all go through this stage... and that's OKAY!" (see link to slides above).  

![xkcd comic](https://imgs.xkcd.com/comics/git.png)  

Indeed, git is hard, but the feeling of finally using git commands in the shell (the terminal on your PC or Mac) is unlike any other coding win I have ever experienced! And you can feel the joy, too!  

Having been through a lot of online resources, we've found the following YouTube tutorial most helpful for figuring out using **Git Bash** (that is using git via the **shell**): https://www.youtube.com/watch?v=pDmYNK68IEc ("Learn Git from Scratch - Creating branches and pushing to Github")

To get a better understanding of how git actually works, we strongly recommend this recent R-Ladies talk by Bruna Wundervald: http://brunaw.com/slides/git-workshop/git-workshop.html#1. Her tutorial walks you through: creating a Github account, cloning a **repo**, connecting local git to Github via SSH key, pushing your changes to repo, adding a .gitignore file, contributing to existing repos, brances + and more!  

## Some recommendations for code review in practice
### Tips by Lindsay Peterson  
* Our basic process is this: the 'default' branch should always be run-able, bug-free, and only include code that has been reviewed. Nobody is able to 'push' directly to the default branch. Instead, code authors work on changes in a separate named branch (e.g. if you're making some changes to your stimuli, the branch might be called "stim_changes"). Once a named branch is ready, the author creates a 'pull request' on Github which starts the code review process.  
* It's worthwhile using a tool that will *check your code* for errors and check the quality of the code. We use 'Pylint' (https://www.pylint.org/) to help catch bugs in new code before it is integrated into the default branch.  
* Have a *common formatting style* for your lab's code. It is easier to understand and review code if it is written in a consistent style. Again, use a tool to help with this. For us, all code must be run through 'Black' (https://github.com/psf/black) before it is submitted for a code review.  
* Try to keep each review relatively small and limited to one issue/thing.  
* Google's guidelines on how to do a code review are quite good: https://google.github.io/eng-practices/review/reviewer/  

### Tips by Angie Jones
* ...
https://techbeacon.com/app-dev-testing/10-commandments-navigating-code-reviews

## Practical demo with Rosanne & Anna (live code review)
Here Rosanne and Anna will provide a live demonstration of reviewing a small R-Script with git (can be found in this repo).  

## Glossary
**Git** = the most widely used modern version control system in the world today (originally developed in 2005 by Linus Torvalds). Via [Bruna Wundervald](http://brunaw.com/slides/git-workshop/git-workshop.html#5)

**Github** = a web-based hosting service for version control using git (it's like a "social network" for git. Via [Bruna Wundervald](http://brunaw.com/slides/git-workshop/git-workshop.html#5)

**Git Bash** = Git Bash is an application for Microsoft Windows environments which provides an emulation layer for a Git command line experience. Bash is an acronym for Bourne Again Shell. A shell is a terminal application used to interface with an operating system through written commands. (from: [Atlassian](https://www.atlassian.com/git/tutorials/git-bash) )

**Repo** = Github repository

**Shell** = In computing, a shell is a user interface for access to an operating system's services. In general, operating system shells use either a command-line interface or graphical user interface, depending on a computer's role and particular operation. (from: [Wikipedia](https://en.wikipedia.org/wiki/Shell_(computing)))  

## Further reading
* An interesting paper on improving reproducibility of scientific code (as opposed to developing production software): "Re-run, Repeat, Reproduce, Reuse, Replicate: Transforming Code into Scientific Contributions" by Benureau & Rougier (2018). Link: https://www.frontiersin.org/articles/10.3389/fninf.2017.00069/full
* Git cheat sheet: https://www.atlassian.com/git/tutorials/atlassian-git-cheatsheet 
* "Git light" - using git directly in RStudio: http://www.geo.uzh.ch/microsite/reproducible_research/post/rr-rstudio-git/
