---
title: "How to set up your own (academic) website using Nene"
date: 2022-09-05
---

>> Work in progress. For now mostly for testing purposes

Having a website is the perfect way of determining the way people see you on the internet. Especially in academia, it allows you to introduce tourself on your own terms and add context to your published papers and presentations. 

This blog post gives a quick introduction to building your own website using the static site generator [Nene](https://nene.leouieda.com/) provided by [Leonardo Uieda](https://www.leouieda.com/) as one of his many phenomenal open-source projects. A brief disclaimer before we start: The following instructions assume you are working on Linux and are somewhat familiar with it as well as git. Using WSL makes it fairly straightforward to use the same instructions on Windows. 

The first thing you need to start is to install Nene on your local machine to develop your website locally by pushing every new content directly to the live page. Nene is a Python package and you can therefore install it straightforwardly using [anaconda](https://www.anaconda.com/products/distribution) using 

```python
conda install nene -c conda-forge
```

if you want to use pip or have some more information on the dependencies look [here](https://nene.leouieda.com/install.html).

No that you have Nene installed you can build you website using the command:
```python
nene
```

If you want to see it in your browser for local development using:
```python
nene --serve
```

But this command alone wont give us a website. To do that we need to provide Nene with a folder of markdown, css and html files. If you are like me and barley know what those are there is an easy way to get a working structure that you can adapt to your needs. I used the github template function to get a copy of Leonardos [website]](https://www.leouieda.com/) and use it as a starting point. You can also use one the websites listed on the [Nene webpage](https://nene.leouieda.com/manual/) if you like their looks more.

To make get a template got to the gitpage containing the source files, e.g. https://github.com/leouieda/website and press the big green 'use this template' button in the top right. This allows you to have a fork of the website in your own github profile. 

