---
layout: post
title:  "Get started with Jekyll"
date:   2019-04-24 15:42:00 +1200
categories: jekyll update
---
Hi there! You may be interested in this series of blog posts to learn how to build a site using Jekyll.

I'm writing as if you have similar amounts of knowledge to web development as me:
* Completed a web development boot camp, e.g. [Enspiral Dev Academy](https://devacademy.co.nz/)
* Built some nodeJS CRUD (create read update delete) apps
* Deployed those apps and their datastores locally and on a platform such as [Heroku](https://www.heroku.com/)

I'm always learning, and I hope by sharing what I've learnt (and how 've learnt it) that you pick up something new along the way as well :smile:

For reference's sake, I am using a MacBook with macOS Mojave 10.14.4. I'm confident this walkthrough will be similar on an FOSS operating system such as Ubuntu. I can provide _some_ support for Windows 10/WSL, but I'm not as confident in that area since changing over to a Macbook.

## Getting ready for Jekyll

One drawback of documentation out there on the web is that it's written with undocumented assumptions about the reader. I found the Jekyll docs were well-pitched to someone who had a development set up that had been through the gauntlet of different languages and frameworks. As for my MacBook, well... the relationship between it and me is still relatively new as I made the change from a Surface Pro 4 only a couple of months ago.

Here's what I needed to do to get Jekyll running locally.

Note: I didn't use `sudo` unless the scripts specifically asked to be executed with `sudo` permissions.

### Installing Homebrew

When I started using macOS, I didn't even know I needed a package manager. Homebrew - or Brew - is a popular package manager for new starters to macOS.

I pasted and executed the following script into my terminal:

{% highlight shell %}
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
{% endhighlight %}

And that was it! Brew installed. Read more about Brew and its delights at [brew.sh](https://brew.sh/)

### Installing Ruby

Now that you have Brew, you can install Ruby with:

{% highlight shell %}

$ brew install ruby

{% endhighlight %}

Boom. In either a later revision or a separate blog post, I'll provide a comparison of how to use Ruby if you're use to using Node and its package managers (either `npm` or `yarn`).

If you are using a different package manager, check out the installation guides on [ruby-lang.org](https://www.ruby-lang.org/en/documentation/installation/)

### Installing Jekyll

We're about to get the [pièce de résistance](http://en.brickimedia.org/wiki/Piece_of_Resistance) by installing Jekyll.

{% highlight shell %}

$ gem install bundler jekyll

{% endhighlight %}

### Create a new Jekyll project

Now that you've installed Jekyll, you will be able to build a new Jekyll-based project. When you create a new project, Jekyll will create a directory and the initial scaffolding (i.e. the files needed to start the foundations of your project) in it.

To create your new Jekyll project:

{% highlight shell %}

$ jekyll new my-new-blog

$ cd my-new-blog

{% endhighlight %}

Have a look through your directory, and you should see a list of files and directories created to get you started.

I'll talk through what's in the directory in another post.

You should see that the Jekyll project is working for you. Run the following command to get your Jekyll site going:

{% highlight shell %}

$ bundle exec jekyll serve

{% endhighlight %}

This runs your Jekyll site locally on port 4000 by default. Browse to http://localhost:4000 in your web browser, and you should see a basic Jekyll site, waiting for your content and creativity to fill it!
