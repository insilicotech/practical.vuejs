---
video_id: 01-Learning-Vue-Hello-Databinding
date: 2018-02-22
title: VueJS Startup
categories:
  - VueJS
description: VueJS Startup
type: Document
---
A Vue instance can also be thought of as a [ViewModel](https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93viewmodel) in the MVVM pattern.

Vue provides two approaches for doing the two-way data binding.

* Fluid template expression (double curly brackets)
* Customized directive("v-model" Vue directve)

Vue Make you decompsing DOM junk inoto hierachical stucture implemented by following Vue Component.

* Conditional visibility controll by "v-show"
* Exclusive visibility controll by "v-if"/"v-else"
* Display elements iterativly by "v-for"/Filterby, Orderby

For interactivity, "v-on" directive(shorthand "@") for listening on DOM events.

## Features of Vue.js

* Declarative Rendering

~~~ markdown
<div id="app">
  {{ message }}
</div>
~~~

~~~ javascript
var app = new Vue({
  el: '#app',
  data: {
    message: 'Hello Vue!'
  }
});
~~~

* Dynamic Data-Binding

~~~ html
<div id="app2">
    <span v-bind:title="message">Hover your mouse over me a few seconds.</span>
</div>
~~~


``` javascript
var app2 = new Vue({
    el: '#app2',
    data: {
        message: 'You load this page on ' + new Date().toLocaleDateString()
    }
});

```


### Installation

The Jekyll gem makes a `jekyll` executable available to you in your Terminal window. You can use this command in a number of ways:

~~~ bash
$ jekyll build
# => The current folder will be generated into ./_site

$ jekyll build --destination <destination>
# => The current folder will be generated into <destination>

$ jekyll build --source <source> --destination <destination>
# => The <source> folder will be generated into <destination>

$ jekyll build --watch
# => The current folder will be generated into ./_site,
#    watched for changes, and regenerated automatically.
~~~

## Fundmental of Jekyll

### Core Concept

Jekyll is a simple, blog-aware, static site generator. It takes a template directory containing raw text files in various formats, runs it through a converter (like Markdown) and our Liquid renderer, and spits out a complete, ready-to-publish static website suitable for serving with your favorite web server.

Jekyll is, at its core, a text transformation engine. The concept behind the system is this: you give it text written in your favorite markup language, be that Markdown, Textile, or just plain HTML, and it churns that through a layout or a series of layout files. Throughout that process you can tweak how you want the site URLs to look, what data gets displayed in the layout, and more. This is all done through editing text files; the static web site is the final product.

### Directory structure

A basic Jekyll site usually looks something like this:

~~~ bash
.
├── _config.yml
├── _data
|   └── members.yml
├── _drafts
|   ├── begin-with-the-crazy-ideas.md
|   └── on-simplicity-in-technology.md
├── _includes
|   ├── footer.html
|   └── header.html
├── _layouts
|   ├── default.html
|   └── post.html
├── _posts
|   ├── 2007-10-29-why-every-programmer-should-play-nethack.md
|   └── 2009-04-26-barcamp-boston-4-roundup.md
├── _sass
|   ├── _base.scss
|   └── _layout.scss
├── _site
├── .jekyll-metadata
└── index.html # can also be an 'index.md' with valid YAML Frontmatter
~~~

### Front matter

The front matter is where Jekyll starts to get really cool. Any file that contains a YAML front matter block will be processed by Jekyll as a special file. The front matter must be the first thing in the file and must take the form of valid YAML set between triple-dashed lines. Here is a basic example:

~~~ html
---
layout: post
title: Blogging Like a Hacker
---
~~~

Between these triple-dashed lines, you can set predefined variables (see below for a reference) or even create custom ones of your own. These variables will then be available to you to access using Liquid tags both further down in the file and also in any layouts or includes that the page or post in question relies on.

![Example image](https://images.unsplash.com/photo-1481487196290-c152efe083f5?ixlib=rb-0.3.5&q=80&fm=jpg&crop=entropy&cs=tinysrgb&w=1920&h=1080&fit=crop&s=80308172730757a7db0434987fa985f3)

## Reference

* [尤雨溪(Vue.jsChief Procrastination Officer)](https://www.zhihu.com/people/evanyou/activities)
* [CTOLib码库->Javascript](https://www.ctolib.com/javascript/docs/)
* [Awesome-Vue](https://github.com/vuejs/awesome-vue)

### coligoシリーズ

1. [VueJs: The Basics](https://coligo.io/vuejs-the-basics/)
2. [VueJs: The Basics](https://coligo.io/vuejs-the-basics/)

