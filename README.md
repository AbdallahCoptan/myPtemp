![By AbdallahCoptan](https://img.shields.io/badge/by-AbdallahCoptan-blue.svg) [![github](https://img.shields.io/badge/git-github-lightgray.svg)](https://github.com/AbdallahCoptan/myptemp) [![Issues](https://img.shields.io/badge/issues-github-green.svg)](https://github.com/AbdallahCoptan/myptemp/issues)

                         _____  _                       
                        |  __ \| |                      
         _ __ ___  _   _| |__) | |_ ___ _ __ ___  _ __  
        | '_ ` _ \| | | |  ___/| __/ _ \ '_ ` _ \| '_ \ 
        | | | | | | |_| | |    | |_  __/ | | | | | |_) |
        |_| |_| |_|\__, |_|     \__\___|_| |_| |_| .__/ 
                    __/ |                        | |    
                   |___/                         |_|    
       Copyright (c) 2020 Abdallah Ibrahim <abdallah.cisco@gmail.com>

This is my Beamer

## Installation / Repository Setup

This repository is hosted on [Github](https://github.com/AbdallahCoptan/myptemp).

* To clone this repository, proceed as follows (adapt accordingly):

```bash
$> mkdir -p ~/git/github.com/
$> cd ~/git/github.com/
$> git clone git@github.com:AbdallahCoptan/myPtemp.git
```


**`/!\ IMPORTANT`**: Once cloned, initiate your local copy of the repository by running:

```bash
$> cd myptemp
$> rake setup
```

This will initiate the [Git submodules of this repository](.gitmodules) and setup the [git flow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow) layout for this repository. Later on, you can update your local branches by running:

     $> rake up

If upon pulling the repository, you end in a state where another collaborator have upgraded the Git submodules for this repository, you'll end in a dirty state (as reported by modifications within the `.submodules/` directory). In that case, just after the pull, you **have to run** `make up` to ensure consistency with regards the Git submodules:

Finally, you can upgrade the [Git submodules](.gitmodules) to the latest version by running:

    $> rake git:submodules:upgrade
## Compilation of the LaTeX sources

The compilation of this document relies on [GNU Make](http://www.gnu.org/software/make/), and you should have a complete working LaTeX environment (including the `pdflatex` compiler).

To compile this document, simply run:

	$> make

This shall generate the PDF version of the document


## Issues / Feature request

You can submit bug / issues / feature request using the [`AbdallahCoptan/myptemp` Project Tracker](https://github.com/AbdallahCoptan/myptemp/issues)



## Advanced Topics

### Git

This repository make use of [Git](http://git-scm.com/) such that you should have it installed on your working machine: 

       $> apt-get install git-core # On Debian-like systems
       $> yum install git          # On CentOS-like systems
       $> brew install git         # On Mac OS, using [Homebrew](http://mxcl.github.com/homebrew/)
       $> port install git         # On Mac OS, using MacPort

Consider these resources to become more familiar (if not yet) with Git:

* [Simple Git Guide](http://rogerdudler.github.io/git-guide/)
* [Git book](http://book.git-scm.com/index.html)
* [Github:help](http://help.github.com/mac-set-up-git/)
* [Git reference](http://gitref.org/)

At least, you shall configure the following variables

       $> git config --global user.name "Your Name Comes Here"
       $> git config --global user.email you@yourdomain.example.com
       # configure colors
       $> git config --global color.diff auto
       $> git config --global color.status auto
       $> git config --global color.branch auto

Note that you can create git command aliases in `~/.gitconfig` as follows: 

       [alias]
           up = pull origin
           pu = push origin
           st = status
           df = diff
           ci = commit -s
           br = branch
           w  = whatchanged --abbrev-commit
           ls = ls-files
           gr = log --graph --oneline --decorate
           amend = commit --amend

Consider my personal [`.gitconfig`](https://github.com/Falkor/dotfiles/blob/master/git/.gitconfig) as an example -- if you decide to use it, simply copy it in your home directory and adapt the `[user]` section. 

## Contributing

That's quite simple:

1. [Fork](https://help.github.com/articles/fork-a-repo/) it
2. Create your own feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Added some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new [Pull Request](https://help.github.com/articles/using-pull-requests/)
