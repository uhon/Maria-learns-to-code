# Maria learns to code
...for Maria and everyone else interested in Web-Programming

- Table of Content
  * [Saludos](#saludos)
  * [Introduction](#introduction)
  * [Frontend](#frontend)
    + [Styling](#styling)
      - [CSS](#css)
      - [Alternatives](#alternatives)
      - [Bootstrap](#bootstrap)
      - [Want an icon?](#want-an-icon)
    + [Programming](#programming)
      - [Jquery](#jquery)
      - [Ajax (XmlHttpRequest)](#ajax-xmlhttprequest)
    + [Alternatives to Javascript](#alternatives-to-javascript)
    + [Building](#building)
  * [Backend](#backend)
    + [PHP](#php)
    + [Ruby](#ruby)
    + [Scala](#scala)
  * [Bash!](#bash)
  * [Hosting](#hosting)
  * [Collaboration](#collaboration)
  * [Hello World](#hello-world)
  * [Share this!](#share-this)

## Saludos
Hi Maria, as promised here come the web-programming-advices from the wise old (little drunk) guy.
As you can see, i published it on github, since it shall be accessible by any girl (or boy) who wants to learn to program.

If you Maria, or anyone else wants to extend this guide, "fork" this repository and send me a pull-request once you're done. Lets see where this goes.

This documentation is written in markdown-format (the text-format of choice for documenting programming-related stuff). The documentation is actually a file called README.md sitting at the root-directory of your github repository (if you want to see its markup, open it in RAW-Mode). It is easy to collaboratively work with Markdown (since it is text) and github formats it nicely as you can see.

## Introduction
One important thing first. Learning the programming languages is one, but it is much more important to familiarize yourself with frameworks and the technology-stack around it.
Frameworks make your live much easier and at the same time, they make you use the languages on a decent level while working with them. So after you familiarized yourself with the most basic language-constructs, you should dive into the world of frameworks.

The advices I give you below are based on my own experiences and are the things i can truly recommend to anyone who wants to start programming. Although I think (not all of them, especially javascript and php) are the most elegant technologies to work with, but for sure quite easy to start with. Also the job opportunities are quite good when you know them.

For any of those technologies described, there are various tutorials, first-step-guides and sample-application on github, just use the search.
For documentation, check the official website of the respective technology. I'm too lazy to link those here, but I'm sure you will find them

You may also follow the technology or framework related subreddit on reddit.com (and if you want to read some programming-related jokes, head over to: reddit.com/r/ProgrammerHumor)

## Frontend

### Styling
If you want more than just text...

#### CSS
Web-Browsers use CSS (and only CSS) for styling websites. Key here is that you write stylesheets (is more about configuration than actuall programming) where you define which element have which styling properties (mapped via class-attribute of the html-tags which you want to style)
 
#### Alternatives
Although Browsers only understand CSS, you can use other approaches to style your website, namely 
* less 
* sass

those languages are almost identical to CSS, but allow to bring in variables, nest elements and do basically all the complicated stuff for which you would write books of configuration in CSS.
Attention: Less and Sass need to be compiled to CSS. This can be done with the technologies described under Building

#### Bootstrap
If you want your website to look nice, use Bootstrap.
When using it, it is very easy to make a nice looking Website (even interactive with Tabs, Modal-Dialogues and so forth)
It features a Grid-Layout (with 12 rows) so you can scale your containers (divs) as you want. Like 6/12 on laptop screen and 12/12 on mobile (this is called "responsiveness")

#### Want an icon?
Don't use images! If you want to use free icons to display on your page, you can go with
* font-awesome 
* glyphicons

They offer hunderets of free scalbable icons, provided as font (vector-graphics). Inserting an icon is as easy as 
```html
<i class="fa fa-iconOfYourChoice" />
```

### Programming
You have no choice, its Javascript (deal with it, or do better with one of the alternatives described below)
Luckily there are many tools around Javascript which make your live easier. Especially Jquery. 

#### Jquery
Although it is kind of an old-fashioned technology, it is really convenient and offers a huge range of plugins which do fancy stuff with your web-page.
Wanna start something right after your website finished loading, use this construct:
```javascript
$(function() {
	// your code here, do something like:
	$("#myCoolNewElement").fadeIn();
});
```

#### Ajax (XmlHttpRequest)

This is a technology to communicate with a Backend-Server to fetch information without a reload of the page. You can load parts of your Website dynamically, or update them in place, without a flickering of the website, since there is no reload. Use Jquery to conveniently use its power

### Alternatives to Javascript
There are dozens, like:
* Typescript
* Coffeescript
* Go
* Scala.js
* Elm

My Favorite is Scala.js (Using Scala on Front and Backend gives me many new possibilities), nevertheless I'd recommend you make yourself familiar with Javascript before diving into languages which compile to Javascript

### Building
If you serve a website, you want to make sure everything is delivered nicely, so ideally you want to serve only one Javascript-File and one CSS-File (instead of one file for every library you are using, because there is a HTTP-Request for every file you link with script or link-tag).
Use one of those Building-Frameworks:  
* grunt
* gulp

to bundle together all your assets (stylesheets and javascripts) and deliver them for your website. 
It also provides plugins to compile less (or sass) files, does javascript-linting (checking the code for errors) and distribute it as a minified version.
Building is part of the development-cycle. So it must happens before you call your website (your html-code only contains references to the builded js or css files)

## Backend
Wow i don't know where to start. Seriously, there are just too many technologies you can use on the backend side. 

### PHP
One of the most used Web-Languages is PHP and there are many good and powerful opensource-solutions written in it. Like Wordpress (blog/cms system), Typo3 (CMS), Moodle (e-learning platform) and many more.
Getting into PHP world is (in my opinion) quite easy since there are so many good examples. And if you don't want to start from scratch, use one of the Opensource-Solutions and extend it with your needs (they are built to extend them and offer good documentation).
If you want to make a decent Web-Application, use a framework like Symphony (it offers a db-orm-layer called doctrine). This tool at hand, you can do everything you want (except writing elegant code, for this you need something else than PHP)!

### Ruby
Ruby is fun! It comes with a Framework called Rails (so its Ruby on Rails) and has a huge package-system called ruby-gems which solves almost every problem you could stumble upon.
Rails is a Framework following strictly the "Convention over Configuration" paradigm. So if you stick to conventions, it lets you achieve incredible powerful things with less and more beautiful code than in PHP! I'd personally start with ruby if I'm new to backend-development.

### Scala
This is what i do. Its fancy, quite new and built for scalability. Its also the most powerful thing I ever stumbled upon.
It has almost all the benefits of Ruby and can be ussed cross-origin (u can use it on the client (compiled to js) and server). And due to Type-safety it is more error-prone than other languages. The Framework of choice is called play-framework.
Since Scala is not an interpreted language, it must be compiled first. Also Hosting it might be a little more difficult than with PHP and Ruby
Read an introduction to it in German here: http://www.insign.ch/blog/2016/04/11/scala-die-programmiersprache


## Bash!
All technologies described require you to interact with them (set them up) via your Terminal (also called Shell, or Bash on a Linux-based System, including MacOS)
Entering Web-Technologies means, you enter a Linux/Unix World. So throw out your Windows Operation System and start using real stuff. If you are on Mac already, go with that, otherwise use Linux (Ubuntu)

## Hosting
Ok, you did dive into Backend-Programming. Now you need a way to publish your website. There are many Webserver-Solutions. Most important ones are
* Apache
* Nginx (engine X)

This Webservers let you serve your application, whether it is on localhost or on a Linux-Server of your Choice.
If you want to use Scala, it comes with its own webserver called Netty (included in play-framework)

## Collaboration
Make yourself a github account. This is your code-sharing platform of choice and totally free for your code, as long as you don't want to hide it (public repositories are for free). 
But why should you hide your code? All code ever written proves that you are a active developer (especially useful if you are not employed). An your code might even become handy for someone else in the future.
For every Developer Job (no matter if frontend or backend) it is absolutely essential to use a Version-Control-System. And today there is only one reasonable choice called GIT.
Make yourself familiar with it by playing around with the lessons provided here: http://learngitbranching.js.org


## Hello World
Most important advice at the end.
Don't give up! Although it can be a hard and painful process to learn to program, it will definitely reward you with a lot of joy (every time you made something work).
Be creative!

## Share this!
If you know any Girl (or even boy) who wants to learn to program, give her this link.
There are too few girls in IT, lets change it ;) 

