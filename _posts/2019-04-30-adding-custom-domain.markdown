---
layout: post
title:  "Adding a custom domain to your Github page"
date:   2019-04-30 15:33:00 +1200
categories: jekyll create custom domain
---

If you have bought your `.dev` domain via [Porkbun](https://porkbun.com/) like I have, setting up your `.dev` domain for your Github page is quite straight-forward.

[Follow the instructions on this Porkbun knowledge base article.)[
https://kb.porkbun.com/article/64-how-to-connect-your-domain-to-github-pages]

You should also make a CNAME record for your Github repository - the one that is named `[YOUR GITHUB USERNAME].github.io`

Do this with the following script in the root directory of your repository:

{% highlight shell %}

$ touch CNAME

{% endhighlight %}

You don't need to worry about file extensions. Open the file in your code editor of choice, and put in the `.dev` domain name you are using. For example, [in the CNAME record in my repository directory](https://github.com/catherineedwards/catherineedwards.github.io/blob/master/CNAME), I have entered `cedwards.dev`. This should clear any domain-resolution issues with Github.io.