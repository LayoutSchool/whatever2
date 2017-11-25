---
layout: post
title:  "5 Most Important Selectors for CSS Targeting"
date:   2017-10-29 07:58:40 +0200
category: ['code']
comments: true
image: /img/2016/08/09/become-a-finisher.jpg
excerpt_separator: <!--more-->
show: true
aotw: true
---

In this guide, we will look at the most common approaches in targeting HTML elements using CSS. 

Understanding how to target various sections of our HTML using CSS selectors is at the bottom of the frontend developer pyramid (a fun way to separate front end developers by knowledge/experience).    

Targeting is also crucial for understanding other concepts when working with CSS. For example, without proper understanding of targeting, we'd have difficulty understanding BEM (Block, Element, Modifier) notation, or SMACSS way of organizing our CSS.

<!--more-->

<h3>1. Universal Selector</h3>
The universal selector is a catch-all selector, meaning it will target all elements on the page (except pseudo classes). What follows is an example from Bootstrap 4 beta 2:
<div class="bg-light-gray p-3">
{% highlight css lineos %}
    *,
    ::after,
    ::before {
        box-sizing: border-box
    }
{% endhighlight %}
</div>

<h3>2. Type Selector</h3>
This selector targets the element itself. An example from Bootstrap 4 beta 2:
<div class="bg-light-gray p-3">
{% highlight css lineos %}
  html {
      font-family: sans-serif;
      line-height: 1.15;
      -webkit-text-size-adjust: 100%;
      -ms-text-size-adjust: 100%;
      -ms-overflow-style: scrollbar;
      -webkit-tap-highlight-color: transparent
  }
{% endhighlight %}
</div>

<h3>3. ID Selector</h3>
This selector targets the id attribute in your HTML. For example you could have the following HTML:
<div class="bg-light-gray p-3">
{% highlight html lineos %}
  <h1 id="page-title">...</h1>
{% endhighlight %}
</div>

To style <em>only</em> the above html element, we can select its id attribute as follows:
<div>
{% highlight css lineos %}
  #page-title {
    font-size: 50px;
  }
{% endhighlight %}  
</div>

<h3>4. Class Selector</h3>
This selector targets class attributes in your HTML. For example you could have the following HTML:
<div class="bg-light-gray p-3">
{% highlight html lineos %}
  <p class="page-paragraph">...</p>
{% endhighlight %}
</div>

To style <em>all</em> the p tags with the class attribute of ''page-paragraph'', we can use the following CSS:
<div>
{% highlight css lineos %}
  .page-paragraph {
    font-size: 16px;
  }
{% endhighlight %}  
</div>

<h3>5. Descendant Selector</h3>
This selector is used for several scenarios. We'll look at a couple of examples here:
<ul>
<li>Targeting an HTML element that is located <em>inside</em> another HTML element</li>
<li>Targeting a class that is located inside an html element</li>
<li>Targeting a class that is located inside another class</li>
</ul>

Let's look at our example HTML structure:
<div class="bg-light-gray p-3">
{% highlight html lineos %}
  <article class="article article-main">
    <h2 class="h2 h2-article">An h2 heading</h2>
    <p class="paragraph paragraph-intro">The first paragraph</p>
    <p class="paragraph paragraph-normal">The second paragraph</p>
  </article>
{% endhighlight %}
</div>

Now, let's look at the CSS for each of the listed examples:
<div class="bg-light-gray p-3">
{% highlight css lineos %}
  /* example 1: element inside element */
  article p {
    /* some CSS code */
  }
  /* example 2: a class of an element, inside an element */
  article .paragraph-intro {
    /* some CSS code */
  }
  /* example 3: a class inside another class */
  .article-main .paragraph {
    /* some CSS code */
  }
{% endhighlight %}  
</div>

To fully understand each of the given examples, let's explain how each example of CSS targeting works:

<ul>
  <li>
  Example 1: This code will style all p elements inside the article element
  </li>

  <li>
  Example 2: This code styles any element with the class of .paragraph-intro, that's inside the article element
  </li>

  <li>
  Example 3:This code targets all elements with .paragraph class, inside elements that have the class of .article-main
  </li>
</ul>

[ourblog-theme]: {{ site.url }}/template-overviews/our-simple-blog
