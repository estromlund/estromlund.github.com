---
layout: post
title: First post! (and how you can setup your Jekyll blog on GitHub, too)
---
Testing 1,2,3...am I on?

If this works, then I have successfully deployed a Jekyll blog to [Github Pages](http://pages.github.com) with a
[custom domain](http://blog.erikstromlund.com). As
 a quick
 recap, and for future reference, here's what I had to do:

## Create a new repository
1. Create a new repository on GitHub. This must be named properly in order for everything to work. Specifically,
it must be of the format *username.github.io*. In my case it is [estromlund.github.io](http://estromlund.github.io).

2. Clone the new repo to your local machine:

 ```bash
 git clone git@github.com:estromlund/estromlund.github.io.git
 ```

## Setup your environment
1. You will need Ruby 1.9.3 or 2.0 installed. If you do not have something set up, then I suggest using rbenv. It can
 get rather complicated, but there are many tutorials out there.

2. Next, install the necessary gems, using bundler, by placing the following in your `Gemfile`:

 ```ruby
 source 'https://rubygems.org'
 gem 'github-pages'
 ```

Now run `bundle install`.

## Choose a theme
1. I personally wanted to use a theme from the start, since I don't want to bother with design choices. Thus, I
chose the [Lagom theme](https://github.com/swansom/lagom), but feel free to use what you want. A good source to
browse is [Jekyll themes](http://jekyllthemes.org). To install the theme, simply clone it to your local machine
(doesn't matter where, we will be moving stuff):

 ```bash
 git clone git@github.com:swanson/lagom.git
 ```

2. Now, copy everything from the *lagom* (or your theme's) directory to your Jekyll directory (in our case,
*estromlund.github.io*). If prompted to replace items in the target directory, you probably want to choose Yes.

3. You will want to change some settings now. These are all found in the file `_config.yml`. Anything in there is
accessible to the rest of the blog under the `site.*` namespace. For example, `site.url` will always return the url
you place here, and can be a useful variable in other spots on your blog. If you used a template,
then there are probably a lot of values that you will immediately want to change -- for example,
[I changed](https://github.com/estromlund/estromlund.github.com/blob/master/_config.yml) the URL,
my name, my twitter/linkedin/etc. links, and the default color. Your template may have other values that you will want to change.

## Create your first post
1. At this point, you should have a blog that can be deployed to GitHub. However, lets add a post first. In the root
directory, add a folder called `_posts`. Under this directory, create a file called `2014-02-21-first-post.md`. This
format is required by Jekyll and is `YYYY-MM-DD-short-name-of-your-choice.MARKUP_LANGUAGE`. In our case,
it is a blog post called "First Post", on February 21, 2014, and we will be writing in markdown. Go ahead and open
that file, then add the Jekyll-required YAML-formatted "front-matter", followed by your post's text. This just tells
Jekyll which template to use, and what the blog's title is:

 ```yaml
 ---
 layout: post
 title: First post
 ---
 This is the text in my first post!
```

1. We now have a post and are ready to deploy the blog. This is the easy part:

 ```bash
 git push origin master
 ```

Remember your repository name from earlier? Now we can go to that URL (i.e. http://estromlund.github.io) and see our
blog. Note that this can take up to 10 minutes the first time.

## Serve your blog at a custom domain
Now this is all fine, but I wanted to host my blog at a [custom domain](http://blog.erikstromlund.com). Luckily,
this is pretty easy. In my case, I want this blog to be a subdomain of erikstromlund.com.

1. First, create a new file in your root directory called `CNAME`. In this file, you will need to put in just one
thing -- the root domain you will be using. In my case, my `CNAME` file contains `blog.erikstromlund.com`. That is it.

1. Next, you will need to configure your DNS. This can vary depending on your provider, but in any case,
you will want to create a CNAME record pointing your subdomain (i.e. *blog*) to your github.io URL (i.e. *estromlund.github.io*).

That's it. Now you can go to your custom subdomain and see your blog live!

