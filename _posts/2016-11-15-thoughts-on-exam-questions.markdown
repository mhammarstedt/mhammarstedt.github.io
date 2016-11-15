---
layout: post
title:  "Thoughts on exam questions"
year: 2016
month: November
day: 15th
image:  05.jpg
comments: true
---

As mentioned before, this website was created as a part of examination 1 in the course client-based webprogramming
at Linneaus University. With the assignment, a few questions were to be answered concerning the following subjects.
In this post, I strive to answer them with my own thoughts and reflections on each part.

### Pre-compiling CSS
Pre-compiling your CSS is a quick, easy way of building up your CSS-stylesheets while creating a website.
Having written CSS earlier "the old fashioned way", I quickly came to see the advantages of pre-compiling CSS. First
of all (and perhaps best of all), it allows you to place your CSS in different stylesheets while working, yet still
only producing one joined stylesheet at the end! That does definitely come in handy for more than one reason. It
makes stylizing your website more organized, and will be a God-sent gift when working in group on the same project.
Sure, you can code in separate stylesheets normally too, but that would mean you would have to link all those
stylesheets in the head, and not just one. Of course, the downside of this system is that the joined stylesheet
later on might be hard to find your way in and especially to debug. The different styles in your CSS might also
sometimes be hard to separate into different files -- often different sections nearly overwrites each other and
have strong connections.

Pre-compiling your CSS also offers you a great deal of "special effects" when it comes to the actual code-writing.
Variables, nested CSS selectors, operators and other techniques that will be much appreciated. Things that people
have been missing in the language before. And I must say, these improvements are just that -- improvements! Things
suddenly feel slightly easier and less messy when writing CSS stylesheets.

### Techniques for this project
I have allowed myself to try out as many highlights of pre-compiling CSS as I have seen fit. I have been working with
partials and imports to separate my code into three sections (base, blog and mobile) besides the 'main'-file
with my variables. Of course, that means I have also been using variables, and this to store different colors,
sizes and fonts. I have also come to realize that nested CSS selectors are very practical and therefore been using
them frequently in my stylesheets. With that said, I have yet to explore operators, inheritance and other
interesting aspects, but definitely will do so in time.

### Static site generators
Static site generators (SSG) is a brilliant way of creating websites quickly and with the same (or at least a very
similar) layout for all pages. I would say that it is most efficient for blogs, or websites that at least has a
blog page included. This since, again, static site generators allows you to produce new material on a new
page quickly and easily with no coding effort once the layouts have been completed. Like with pre-compiling CSS, I
really like the fact that you can separate your HTML-documents into different files and they will still just be a
single HTML-file at the end. Once again, this make things well-organized and saves a lot of code. I especially think
this comes well in handy to put the code for <head />, <header /> and <footer /> in separate documents. These tags are
the ones you normally have to copy and paste into all HTML-files -- with SSG, I simply don't have to! Which
I would say saves a lot of time and effort, and we all love when that happens.

An approach that static site generators would not be very suitable for is a website with a layout that differs for
each page or subject, thus defeating the purpose of using static site generators. For this, regular coding would
do the trick a lot better. Again, static site generators are well-suited for simple design projects (or at least
websites with a layout that's used through all pages), usually blogs, that doesn't need any databases for products
or something like it, but just contains simple information and perhaps blog posts.

### Robots.txt
 The robots.txt is a file providing instructions for web robots crawling the web, often sent out by search engines,
but not necessarily. The robots.txt is to be placed in the top-level directory on the web server and determines
which robots to allow access to which files on your website.

For my website I have kept it simple and as follows:

{% highlight ruby %}
User-agent: *
Disallow: /
{% endhighlight %}

This excludes all robots from visiting any of the pages on my website, which I believe is the best alternative for the
time being. For now, I feel like allowing search engines to index my website would be unnecessary. In the future
I intend to change this, but I hope to have made some more improvements on my website until then.

### Humans.txt
The humans.txt is a file containing information about the people behind a website. It should be located right
next to the robots.txt file and is simply a quick, easy way to provide information about the team of creators
as well as contact information and resources.

My humans.txt is as follows:

{% highlight ruby %}
/* TEAM */
Creator: Miranda Hammarstedt
Contact: (email-address)
Github: mhammarstedt
Location: Ljungby, Sweden


/* THANKS */
Name: Linneaus University
URL: www.lnu.se


/* SITE */
Last update: YYYY/MM/DD
Language: English
Standards: HTML5, CSS3
Components: Jekyll, SASS
Software: WebStorm, Git, Illustrator, Photoshop
{% endhighlight %}

In this I have provided the necessary contact information concerning myself (in the text above I have excluded the
email-address to avoid yet another possibility for spam), then directed a special thanks to Linneaus University
for providing me with a reason for creating the website. I have also written down the different softwares,
languages and components used for the project as well as provided a date for the last update (which will of course
change constantly).

### Blog comments
 To allow comments on my blog posts I used something called Disqus. This is an easy way of allowing comments on your
website, simply pasting a universal code into the html on the desired page. Though, in my case, I decided to put
the code for Disqus in a separate document in _includes. This way, I gain full control over where I want to be able
to use comments, and can therefore include Disqus on whatever page I want to. I also added a ’comments’ variable
in my YAML front matter for my blog posts. This allows me to choose on which posts I want to allow comments
in a quick and easy way. Now I simply check in my specified html-layout if there is a page.comments variable,
and if not -- no Disqus! So to make it short, I have used Disqus to implement comments, but still have full
control over where I want to allow them.

### Open Graph
Since social media is just continuously growing these days, it is important to pay attention to this aspect when
creating a website. Open Graph is a series of meta tags to put in your head-tag to allow you to control the
information that will be displayed when someone shares or posts a link to your website. Open Graph offers
numerous alternatives of different meta tags to use, although in my case, I have kept it simple as a start:

{% highlight ruby %}
<meta property="og:title" content="mhammarstedt" />
<meta property="og:type" content="website" />
<meta property="og:url" content="https://mhammarstedt.github.io" />
<meta property="og:image" content="https://mhammarstedt.github.io/img/logo.jpg" />
<meta property="og:description" content="A portfolio page for Miranda Hammarstedt" />
{% endhighlight %}

Sharing on social media might not be the most important aspect to consider for this particular website, therefore
I think these five alternatives are more than enough for now. Perhaps later on I will implement more tags, but
for the time being, I just see no reason as to why I would.

### Final words
So there you have it. Thoughts and reflections on the questions for the first examination in client-based
webprogramming. A little longer than the other blog posts (which is actually a good thing, because then I can see
what a long blog post would look like), but I hope you still made your way through it. And with that, I hope to have
done everything for examination 1 properly.
