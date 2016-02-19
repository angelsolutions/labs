---
layout: post
date: Mon Dec 02 2013 00:04:00 GMT+0000 (GMT Standard Time)
title: Raw data vs. visualisation thumb war?
---


Raw data vs. visualisation thumb war?
=====================================

This all started with a desire to understand how innovation and
knowledge transfer might be taking place amongst two related groups of
people.

Now one way to investigate this topic is to gain an understanding of how
frequently the members of both groups interact, to what degree they
trust each other, reach a consensus and what the characteristics are of
each group member. So I carried out a survey with 40 people recently to
determine who talked to who, how they got on with each other and asked
them questions about their experience in the education industry, what
their roles where, what mental models they held about innovation and how
motivated and challenged they felt in their roles.

For those of you familiar with social network literature we are talking
about tie strength, boundary spanners, knowledge complexity and so on.
Check out Hansen (1999)
[http://www.jstor.org/stable/2667032](http://www.jstor.org/stable/2667032)
for a refresher.

The results got wrapped up in Excel’s excellent statistics package from
which I’m able to study the relationships between the variables in the
survey. But what I really wanted to do was to visualise the social
network. Whilst on the hunt for a suitable statistics package I stumbled
across NodeXL
[http://nodexl.codeplex.com/](http://nodexl.codeplex.com/), which is a
fantastic tool for doing just that.

Just looking at frequency of interaction here is a visual picture of the
network produced by running the survey results through NodeXL.

![image](http://38.media.tumblr.com/6afc98118e8eadc7e1c6cb6ae4936731/tumblr_inline_mx5k4gl67i1s27sgu.png)

It’s pretty but what does it mean? The circles are the people, dark blue
represents one group and light blue the other. The yellow lines show the
interactions between the people. Circle size is a function of the number
of links and the strength of those links.

Carrying out a detailed survey like the one above and integrating the
results into NodeXL is pretty time consuming, however NodeXL has some
modules built in that make this kind of thing easy if you want to study
your twitter network.

[www.Watchsted.com](http://www.Watchsted.com) is a free public site that
makes it easy to access the latest Ofsted Inspections and I wanted a
visual view of its twitter network.

So this is what I did with @Watchsted by following these steps.

1.  Download [http://nodexl.codeplex.com/](http://nodexl.codeplex.com/)
2.  Open NodeXL, on my machine it installed here -\> C:\\Program Files
    (x86)\\Social Media Research Foundation\\NodeXL Excel
    Template\\NodeXLGraph.xltx although you can just click on the start
    menu and type NodeXL into “Search programs and Files” if you’re
    running windows 7.
3.  A workbook should open with multiple sheets called “Edges”,
    “Vertices” and so on. Click on NodeXL in the ribbon at the top.
4.  Click “Import”
5.  Click “From Twitter users network”
6.  Where it says “Add a vertex for each” choose the 2^nd^ option called
    “person following the user”.
7.  Increase the limit to say 200.
8.  Click OK
9.  Follow the process to import from twitter (you may need to copy and
    paste a pin number from twitter and you might get an information
    message about word wrap and performance, just click ok)
10. Now go to Groups in the NodeXL ribbon and choose “Group By Cluster”
11. Now go to Graph Metrics, Select All and click Calculate Metrics.
12. Click Show Graph in the panel on the right.
13. You should now see a graph. However if you want to change the
    circles go to the vertices sheet and change the visual properties of
    each vertex (Color, Shape, Size Opacity, Label, etc). If you want to
    change the lines go to the edges tab and do something similar. 
14. For example to change the circle size so it is relative to the
    number of followers go to the Vertices sheet and enter the following
    formulae into the first row of the size
    column *“=[@Followers]/500”* .Drag the formulae down the column and
    then click refresh graph. This will make the circles bigger for
    those people with the most followers. Hover over the column
    headers (Color, Shape, Size Opacity) to see some helpful comments
    explaining the values you can use. (Note I’ve used 500 to help
    scaling but another number or different technique might be helpful
    for your picture)
15. In the right hand panel you might like to change the algorithm that
    is used to draw the graph. Try “horizontal sign wave” and click “Lay
    out again”. Try changing the Zoom and Scale options as well.
16. If you want to save the graph as an image right click on the graph
    and choose “Save Image to File”

This is the twitter following of @watchsted, the bubble sizes are
proportionate to the number of followers.

![image](http://38.media.tumblr.com/2c350816727427cc163e156cbb138f78/tumblr_inline_mx5k54G2S51s27sgu.png)

The lines above are orange. The easiest way to do that is to go to
“graph options” in the right hand panel and change the “colour” and
“curvature” of the edges (edges are the lines). You can also change
individual edge colour on the edges sheet.

You can go a lot further as well, investigating particular hashtags and
comparing twitter followings, here is an example of @watchsted with me
(@winstanley\_john) and another tweeter, it’s kindof like a venn
diagram.

![image](http://38.media.tumblr.com/beb4cfddd76539aafaac15817251547d/tumblr_inline_mx5k5m8pgk1s27sgu.png)If
you want to show the overlap between two groups then in the NodeXL
ribbon go to “import” -\> “import options” and remove the tick from
*“Clear the NodeXL workbook before the data is imported”* then go back
to import and import the results from another twitter user.

If you want to share your NodeXL image on the NodeXL gallery goto choose
“export” -\> “To NodeXL Graph Gallery”

Oh I did say that this was a “thumb war”. The visualisations are pretty
and its possible to improve them further to show labels and images and
the like. I think the true value in the visualisations is getting a big
picture view of your twitter following and thinking about if you are
reaching the right people. However you might want to refer back to the
raw data within NodeXL to figure out the details.

If you’d like me to knock this up for you then send me a DM on twitter.

\

 

