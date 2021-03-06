Script for using RMarkdown to create scientific manuscripts
================
Jörn Alexander Quent
5 December 2017

Welcome
=======

It is great honour for me to be able to talk to you about using RMarkdown to create scientific manuscripts. My aim today is to convince you to use RMarkdown and to show to you how easy it is to create a very neat document with it. As side note, don't bother to write down any code. It is all updated on my GitHub. Before starting let me present to you the end product. This is an example script I generate for you.

Introduction
============

So, what is RMarkdown? . As the name suggests, it combines R and Markdown. R, as you probably know, is an open source programming language for statistics and data visualisation. Markdown on the other hand is a so called lightweight markup language. You can use those languages to format your text. Being lightweight means that it is much easier to use than LaTex for instance. That being said you are still able to knit RMarkdown files to LaTex files. You are even able to use LaTex to create mathematical formulas. And as you can see here, you are also able to create presentation with RMarkdown.

RMarkdown workflow
==================

![Taken from <http://bioconnector.org/workshops/r-rmarkdown.html>](images/rmarkdown-workflow.png)

Before I continue to talk about the pro and cons of using RMarkdown, I want to spend just one slide to explain to you how RMarkdown works. In RStudio you'll work on your RMarkdown file (.Rmd), where you combine chunks of R code with your text. This file is knit with the help of the R package *knitr* to a Markdown file, which then is converted via Pandoc and LaTex to the final output format, which can be .html, .pdf or .docx.

Pros
====

Why using RMarkdown at all? I would say that the main advantage of using RMarkdown lays in the fact that you can share the whole code used for analysis with the public and journals alongside the text. The other main advantage is that it will help you to achieve higher reproducibility when it come to the analysis. In this context, Nuijten et al. (2016) showed that as many as half of all manuscripts they looked at contained erroneous statistics. RMarkdown helps you to track and avoid mistakes in rounding *p*-values, copy & paste errors as well as forgetting to update statistics when you for instance add a new participant to your data set.

Cons
====

I have to admit to you that are also minor disadvantages. Due to the workflow sometimes things might go wrong when you try to switch between output formats (e.g. from .pdf to .html). You also will find yourself asking for help a couple of times for more intricate stuff for instance on <https://stackoverflow.com>. But don't worry, people are very supportive there. Another annoying thing is that the list of references can only be generated at the end of the script.

YAML header
===========

With that being said, now it is time to show you how little it takes to generate a neat looking manuscript.You always start with an YAML header, which you can see here. In that header you specify a lot concerning the title page and the general layout. For instance the title, author and the abstract, but also the spacing between the lines. You can use the system time as the date. What really important is that you can provide a BibTex file that includes the information used for citation.

R chunks
========

What you see here is the R chunk that follows the header, in which you can load everything you need such as libraries and data. An R chunk is always started with three back quotes ("\`") followed by the letter r in curly brackets sometimes with additional specifications. An R chunk is again ended by three additional back quote.

Analysis
========

In those chunks you can analysis your data and save the results in variables, which can later can be used to access the statistical parameters such as the *p*-values.

Reporting statistics
====================

You can see an example of that here, where I used the function *rValue* and *pValue* that I wrote to extract and round correlation coefficients and *p*-values and report them in the text. With that you will never to a rounding error again and you will be more consistent in what you are doing.

Graphics
========

RMarkdown is also great to render your graphical figures alongside your text. With just a few lines of code as you can see here, you can get to a nice output like this. Note that you can use your result variables to access stuff like the *p*-value.

Tables
======

Similarly, you only need a few lines of code to create tables, which you can use for publication. I find the function *kable* very useful for that but there other ones.

Formulas
========

Another great asset is that you can use LaTex formulas and symbols (e.g. Greek ones) and display them. These are by the way shown while you write them in RStudio.

Citation
========

The last point I want to show you that it is quite easy to use BibTex file to cite articles in your text. Here you see an example file I made up, but most programs such as Mendeley or Zotero have an export function that you can use. With the ID here, you are able to cite this item in your text. Either in everything brackets or directly in the text with only the year in brackets. The list of references is then added at the end of the document.

Thank you
=========

I hope that you got an impression of the versatility of RMardown and I also hope I convinced some of you to try and use RMarkdown. You can use the example script as a starting point but feel we to ask me. Maybe I am able to help. In any case, everything I used for that talk can be found on my GitHub account.

Extra advice
============

Get the correct citation style form <https://github.com/citation-style-language/styles>.
