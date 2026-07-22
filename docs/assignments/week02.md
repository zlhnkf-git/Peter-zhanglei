# 2. Project management

## Assignment
* work through a git tutorial
* build a personal site in the class archive describing you and your final project

## What did I learn this week?

* Overview of version control  
* Overview of Git  
* Initialise a new repository  
* Add remote and push/pull  
* SSH Key  
* Git commit messages  
* Branching  
* Making this website  

This week is quite a challenge for me, because I have never tried web development before. Almost every noun is new to me when I get my gitlab account and open the user interface.

![interface][1]  
What's `git`? What's `gitlab`? What's `markdown`? What's `mkdocs`? What's `CI/CD`? What's `YAML`? ...  
What's the connection between them? What's `gitlab-ci.yml` for? What's `mkdocs.yml` for? How do they let me generate my static web pages? What's the difference between using the built-in functions of gitlab and generating static web pages with HTML? When I browsed [*fabacademys' tutorial*][3] and other related learning materials, new nouns are constantly emerging.  
`Jekyll` `VScode` `Bracket` `Docker` `CSS` `Javascript` `version control`...  
![question][2]  
They are also completely unfamiliar to me, which made me unable to start. I don't know what to learn first. I don't know how to continue to complete my assessment. But I have to learn step by step.  

---
Here is Fiore Basile's [introduction][3] to gitlab in 2019. Which is quite useful and helps me a lot.
## What is git? What is gitlab?  

I followed this [GIT tutorial][4]. Here's a short introduction to the basics of Git that I gleaned from my reading. Essentially how to start a repository, how to connect to a remote repository and secure it with an SSH key, how to add files, commit changes and push to the remote repository.

*  Initialise a new git repository
To start a git repository (local file store):  
`$ git init`
*  Configure the repo using:  
`$ git config --global user.name "put name here" `  
`$ git config --global user.email "put email here"`  
The git add command takes a snapshot of the current state of the repository and adds it to a temporary staging area that git calls the "index" (Git-scm.com, 2019). Essentially bringing it to git's attention.  
* Add a single file to the repository:  
`$ git add index.html`
* Add multiple files to the repository:  
`$ git add index.html main.css image.png`
* Add the entire current directory to the repository:  
`$ git add` 
Committing writes the changes permanently into the history of the index.
* Commit the changes:  
`$ git commit -m "Message here describing commit"`
* Check status of the repository:  
`$ git status`  

I don't think I have to learn all the git commands at once. I will use [git-cheat-sheet][5] for more commands.

### SSH Key

According to the tutorial(install git bash in advance), generate SSH key step by step and add it to my own gitlab account.
![image 2](https://gitlab.fabcloud.org/academany/fabacademy/2020/labs/oshanghai/students/pan-cheng/raw/master/docs/images/week02/SSH_Key.png)  
![image 3](https://gitlab.fabcloud.org/academany/fabacademy/2020/labs/oshanghai/students/pan-cheng/raw/master/docs/images/week02/add_key.png)

In this process, I tried to use git bash. But the terminal is very unfriendly for me who has no experience of computer programming. Later, I tried to use git GUI and Visual Studio Code. Their rich interfaces greatly speed up my learning process and are very easy to use.(It even has Chinese language pack.)  
![image 4](https://gitlab.fabcloud.org/academany/fabacademy/2020/labs/oshanghai/students/pan-cheng/raw/master/docs/images/week02/git_gui.png)  
![image 5](https://gitlab.fabcloud.org/academany/fabacademy/2020/labs/oshanghai/students/pan-cheng/raw/master/docs/images/week02/vscode.png)  

---  
## Markdown
The next thing to learn is how to edit text. I'm recommended to use [*Markdown*][6] as a markup language. Since I have no idea of web development and text editing, the first step is to read through the [tutorial][7] and complete all the [exercises][8].  
![image 6](https://gitlab.fabcloud.org/academany/fabacademy/2020/labs/oshanghai/students/pan-cheng/raw/master/docs/images/week02/Markdown.png)  
After learning to use markdown, I can start to edit my own web page text. That's what you see now. Now I use some basic markdown instructions. Next, I will refer to [this web](https://gitlab.com/gitlab-org/gitlab/blob/master/doc/user/markdown.md#colors) to learn more markdown commands.  
See more info about the Markdown syntax in Useful links- Markdown cheatsheet.

---
## Making this website
After being familiar with *doc* folder and corresponding operations such as adding new dictionary and uploading file, I started to learn mkdocs. In order to understand how my previously edited text files and folders generate my static web pages through `.gitlab-ci.yml`(Here is a useful link for [*gitlab-CI/CD*][9]). I also learned how to use the functions of `mkdocs material` ([Here is the link](https://squidfunk.github.io/mkdocs-material/getting-started/#color-palette))to transform theme and other operations. Because I'm not very proficient in using it now, I decided to continue to try and use this function in the later assignment to enrich my static web pages.  
The major new part of the process for me was the Continuous Integration/Continuous Deployment (CI/CD) pipeline in Gitlab, following the push. In the past I have uploaded files directly to a webserver using FTP, but this method is publishing a site from a cloud git repository. From Gitlab Docs: "GitLab offers a continuous integration service. If you add a .gitlab-ci.yml file to the root directory of your repository, and configure your GitLab project to use a runner, then each commit or push triggers your CI pipeline."  The .yml file is written in YAML and tells the runner what to do, it is stored in the repository root and and when anything is pushed to the repo Gitlab will look for the .yml file and start jobs. I have used the default .yml example for a static site:  
![image 7](https://gitlab.fabcloud.org/academany/fabacademy/2020/labs/oshanghai/students/pan-cheng/raw/master/docs/images/week02/gitlab_CI_yml.png)  
After editing `.gitlab-ci.yml` and `mkdocs.yml`, I can see that my static web page is generated automatically([Here is the link](http://academany.fabcloud.io/fabacademy/2020/labs/oshanghai/students/pan-cheng/)). As the first attempt to generate a static web page in a completely unfamiliar way, and browse a large amount of external resources in a very short time, I feel Satisfy.  

---
## HTML

During this period, I also tried to master some methods of HTML production. So I will continue to try different methods to generate my own static web page on gitlab and complete my assignment with project management.  

---
## Useful links

The tutorials of [How to edit your website](https://class.textile-academy.org/tools/tutorials/gitlab/)  

[Markdown cheatsheet](https://guides.github.com/pdfs/markdown-cheatsheet-online.pdf)  


---
[1]: https://gitlab.fabcloud.org/academany/fabacademy/2020/labs/oshanghai/students/pan-cheng/raw/master/docs/images/week02/20200211133652.png
[2]: https://gitlab.fabcloud.org/academany/fabacademy/2020/labs/oshanghai/students/pan-cheng/raw/master/docs/images/week02/u_3868974892_1613328531_fm_26_gp_0.jpg
[3]: http://fabacademy.org/2018/recitations/gitlab.html#1
[4]: https://www.runoob.com/git/git-tutorial.html
[5]: https://github.github.com/training-kit/downloads/github-git-cheat-sheet/
[6]: https://baike.baidu.com/item/markdown/3245829?fr=aladdin
[7]: https://www.markdownguide.org/getting-started/
[8]: https://www.markdowntutorial.com/
[9]: https://docs.gitlab.com/ee/ci/quick_start/