# Getting Started for Tech People

## Overview

### Components 

Gertrude is a customized Jekyll theme that includes the Javascript library CETEIcean for rendering TEI-XML in the browser and making it accessible to JavaScript via HTML Custom Elements. 

The theme itself is an adaption of Robert Love's [Jekyll/Bootstrap starter project](https://github.com/robertlove/jekyll-bootstrap). The inclusion of Bootstrap means that you can use all of the Bootstrap [classes and styles](https://getbootstrap.com/docs/5.3/getting-started/introduction/) to make a responsive and modern site. 

Gertrude contains custom code for handling person and place names indices and for displaying images via IIIF viewers. The Gertrude documentation details how to customize the code for particular digital edition features. 

Gertrude also contains some [Liquid templating language](https://shopify.github.io/liquid/) within the Jekyll framework for arranging and displaying content on the site. 

## Quickstart steps

1. Install Ruby and Jekyll on your computer.
2. Clone the [Gertrude repository](https://github.com/mackenziekbrooks/gertrude) to your computer.
3. Create a GitHub repo for your project.
4. Commit and push the project to your new repo. 
5. Customize and develop platform to your liking. 
6. Deploy the digital edition to GitHub pages or another host. 

## Installing Ruby + Jekyll on Mac

Start with Jekyll's [instructions](https://jekyllrb.com/docs/installation/macos/). 

They also recommend this document on [The fastest and easiest way to install Ruby on a Mac in 2025](https://www.moncefbelyamani.com/how-to-install-xcode-homebrew-git-rvm-ruby-on-mac/) which is truly the most thorough walk-through you will find. You don't have to purchase the paid solution. 

You might also check out [CollectionBuilder's](https://collectionbuilder.github.io/) [documentation](https://collectionbuilder.github.io/cb-docs/docs/software/) on installing Ruby and Jekyll. 

The biggest issue when setting up a development environment is ensuring that all versions of the software you're installing on your computer can work together peacefully. Ruby is a programming language that comes with particular versions. Jekyll is a Ruby **gem**, or code library, and it requires a number of other gems to function (once you're set up, you can see all of them in the file called `Gemfile`). These code libraries are updated all the time and depend on other code libraries to have certain functions. The most troubleshooting you'll encounter will be reconciling these issues via the Stack Overflow method of Googling an error message and trying a solution. 

## Installing Ruby + Jeykll on Windows 

Let's be honest: front-end web development is not easy on a Windows machine. It should only be attempted if you're confident in your abilities. 

[Git Bash](https://gitforwindows.org/) is a tool that allows you to run git from the command line in a way that is similar to the Mac (or Linux) experience. 

[Windows Subsystem for Linux](https://learn.microsoft.com/en-us/windows/wsl/about) is another option for creating a more friendly environment. 

