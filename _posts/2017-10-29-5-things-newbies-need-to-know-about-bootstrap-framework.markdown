---
layout: post
title:  "5 Things Newbies Need to Know About Bootstrap Framework"
date:   2017-9-29 09:18:40 +0200
category: ['code']
comments: true
image: /img/2017/09/02/5-things-newbies-need-to-know-about-bootstrap-framework.png
excerpt_separator: <!--more-->
show: true
aotw: false
---

Bootstrap is the most popular frontend framework in use today. If you are a striving frontend web developer, this post will look at Bootstrap framework from the bird's eye view. 

In this article, we will discuss the 5 most important things that newbies need to know about Bootstrap, namely: the 12-column grid, Sass-based css, the concept of components, extending with jQuery plugins, and a simple way to extend Bootstrap's default classes.

<!--more-->

<h3>1. The 12-column Grid</h3>

One of the reasons for Bootstrap's success is that it solved one of the major painpoints that troubled frontend development during the rise of mobile browsing. The introduction of such tiny viewports demanded a new approach to how websites would be displayed on such limited space. 

The concept of the 12-column grid, first introduced by 960.gs, was already widespread. What set Bootstrap apart at that time was the brilliant application of a straightforward CSS naming convention for responsive grid. 

Even today, one of the most important Bootstrap concepts to understand is the 12-column responsive grid. 

Want to learn more? Watch the free mini-course on Bootstrap's 12-column grid.

<h3>2. Sass-based CSS</h3>

Bootstrap 3 was based on the Less pre-processor. In Bootstrap 4, this was replaced with Sass pre-processor. Therefore, understanding what Sass is and how it works is of great importance for a newbie frontend developer.

A well-known aspect of the human psyche is the fear of the unknown. Understandably so, because during the majority of human history and pre-history, the unknown was usually a synonym for danger. Thus, the fear of the unknown is hard-wired into our biology. It is then fully understandable that initial response to hearing about new technology is usually one of these two:
<ul>
    <li>
        "I've got no idea what that is. It will take me ages to understand it. It's so complicated!", or
    </li>
    <li>
        "I don't need to know everything anyway. I'll just stick with what I know already."
    </li>
</ul>

Both of the responses above are totally unnecessary. The most important thing to understand about Sass is: <strong>you can use <em>only</em>plain CSS inside it</strong>. You don't ever need to use Sass in your Sass files!

What this means is that basically, you can just rename your CSS files to SCSS files.

And this should be your starting point. To begin working with Sass, you should simply take your existing stylesheet and separate it into <em>includes</em>, or <em>partial</em> files. 

Then just let Sass recompile everything back to one file. The advantage of this approach is that there is almost no learning curve. The only thing you need to learn is how to install Sass on your system, and how partial files and Sass compilation work. 

To learn more about this, watch our mini-course: Introduction to Sass for Bootstrap 4.


<h3>3. The Concept of Components in Bootstrap</h3>

<blockquote class="blockquote">
    <p class="mb-0">You're still writing vanilla HTML? My friend, we've got a component for that.</p>
    <footer class="blockquote-footer">Anonymous <cite title="Source Title">Bootstrap Developer</cite></footer>
</blockquote>

Everything in Bootstrap revolves around components. Bootstrap 4 uses the following components:
<ul>
    <li>
        Alerts
    </li>
    <li>
        Badge
    </li>
    <li>
        Breadcrumb
    </li>
    <li>
        Buttons
    </li>
    <li>
        Button group
    </li>
    <li>
        Card
    </li>
    <li>
        Carousel 
    </li>
    <li>
        Collapse
    </li>
    <li>
        Dropdowns
    </li>
    <li>
        Forms
    </li>
    <li>
        Input group
    </li>
    <li>
        Jumbotron
    </li>
    <li>
        List group
    </li>
    <li>
        Modal
    </li>
    <li>
        Navs
    </li>
    <li>
        Pagination
    </li>
    <li>
        Popovers
    </li>
    <li>
        Progress
    </li>
    <li>
        Scrollspy
    </li>
    <li>
        Tooltips
    </li>
</ul>

Knowing what components exist in Bootstrap are a starting point for a newbie frontend developer. 

Most of these components can be just copy-pasted from the official documentation and they will work, so that's a great way to get familiar with the Bootstrap framework.

If you'd like to learn more, watch our free course on Bootstrap components.


<h3>4. Extending Bootstrap with jQuery Plugins</h3>

Once you know about Bootstrap components, you will also know which components do not exist in Bootstrap. 

One example is the range input. 

So, if you need to use it in your layout, you need to either roll out your own, or plug and play one of the many already existing solutions. 

Since Bootstrap's JavaScript is based on jQuery, you should not have a hard time including custom jQuery plugins in your Bootstrap projects.

To learn more about adding a jQuery plugin to a Bootstrap project, watch this video.

<h3>5. Extending Bootstrap's default classes with Sass</h3>

Let's say you want to slightly tweak a bootstrap button. Sass gives us a wonderful way to do just that: the @extend.

What follows is a simple snippet of code that will extend the existing Bootstrap button and add it some additional styles:

<div>
{% highlight scss lineos %}
  .button { // our custom button class
    @extend .btn;
    font-size: 30px;
  }
{% endhighlight %}  
</div>

Once the SCSS code compiles into CSS, you'll get a new class that did not exist in Bootstrap, called .button. The class will have all the CSS declarations that the default Bootstrap class of .btn has, plus the font-size of 30px.

Check out the [Our Blog][ourblog-theme] bootstrap theme to see an example of a layout where this is implemented.

[ourblog-theme]: {{ site.url }}/template-overviews/our-simple-blog
