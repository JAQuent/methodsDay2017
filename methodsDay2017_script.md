Script for Using RMarkdown to create scientific manuscripts
================
Jörn Alexander Quent
28 November 2017

Introduction
------------

My aim for this talk is two fold: first I shortly want to convince you why you should use RMarkdown (or another notebook) and second I want to help you to get started with RMarkdown, which is really versatile tool.

What is RMarkdown? R is an open source programming language for statistics and data visualisation. It is modular in nature meaning that a lot of different packages can be installed to fit your specific needs. Markdown on the other hand is so called lightweight markup language, which can be used by you to format your text. It is much easy to use than LaTex. However you are able to knit RMarkdown files to LaTex files but also PDF or word files. You are even able to use LaTex to create mathematical formulars. As you can see here, you are also able to create presentation with RMarkdown. I will focus on scientific manuscripts, though.

Pros and cons
-------------

Before I start to show you the *relative ease* with which you can create a scientific manuscript. Let me first elobaroate on pros and cons of RMarkdown.

Pro:

-   Reproducibility: RMarkdown can be used to make scientific analysis more reproducible. You will this easily why this the case in the short demonstration.
-   Track and avoid mistkakes
    -   Rounding p-value
    -   Copy & paste errors
    -   Forgetting to up update a particular statistic.

Contra:

-   Sometimes things go wrong when you try to knit a document to .html file, when it was written to be knit a .pdf file (see workflow).
-   You will frequently need to ask for help for more intricate stuff for instance on <https://stackoverflow.com>

RMarkdown workflow
==================

![Taken from <http://bioconnector.org/workshops/r-rmarkdown.html>](rmarkdown-workflow.png)

Tips and tricks
---------------