# TO-DO LIST WITHOUT JS
Simple HTML+CSS page to add and delete tasks

## Table of contents
* [Technologies](#technologies)
* [Setup](#setup)
* [Features](#features)
* [Sources](#sources)
* [Devlog](#devlog)
	
## Technologies
Project is created with:
* HTML
* CSS
	
## Setup
To run this project, clone repo and click index.html file.
Test app in my [codepen](https://codepen.io/Panelinio/pen/GRaxQZP)

## Features
* Add and delete your tasks

## Sources
What helped me:
* [codersblock.com](https://codersblock.com/blog/checkbox-trickery-with-css/)
* [moderncss.dev](https://moderncss.dev/pure-css-custom-checkbox-style/)
* [Pasja Informatyki](https://forum.pasja-informatyki.pl/)
* [aditus.io](https://www.aditus.io/aria/aria-label/)
* [mdn](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value/light-dark)
* Chat-GPT - kinda...

## Devlog
Here is my devlog :D

21.06.2024 - start

So my task is to do... a TO-DO list. But tricky part is that I need to build it without using JS. It sounds like a tough challenge :D

We are going to use HTML forms to display and hide list elements.

Well, I created 2 files - index.html and style.css. I want my app to be darkish. I found pretty-looking colors in [colorhunt.co](https://colorhunt.co/palettes).
Now we need to make that project to be semantic, so instead of using <div> or <table> we are going to use <main>, <footer> etc.
But how to center my elements? With simple CSS attributes :D

Unfortunately I couldn't center list elements... I searched couple of forums but nothing helped me. So I asked Chat-GPT.
Using AI isn't my keen, but it helps me discover new routes and understand what code represents.
Chat-GPT gave me a sollution :D Now to the tricky part - inserting user's tasks in list elements.

And I thought that's not possible. Yet we can't manage dynamic content using only HTML or CSS. But I will find a solution.

So, that seems impossible. I've found a [git repo](https://github.com/kevin-powell/todo-list-collab) that isn't working (or I can't properly launch it).
Even AI is telling me to use PHP.
Welp, that's a solution too. But not here. We are going to use only HTML and CSS no matter what!

And I think I have one way to solve our problem - using only form.
Well, we can create a form with 10 clear labels to put tasks. Clicking on checkbox will remove them.

OK, I FOUND A SOLUTION!
We are going to create couple of empty text inputs and then we use relation in css
```css
.new-task
{
    /*task's style*/
    text-decoration: none;
}

input:checked + label .new-task
{
    text-decoration: line-through;
}
```
```html
<input type="checkbox" class="task-box" id="task-1"/>
    <label for="task-1">
        <input type="text" class="new-task"/>
    </label>
```

Now after clicking on checkbox we can delete our task :D
So we can already add some animations and make that page responsive. Done :D


24.06.2024

I published my work to Polish forum - Pasja Informatyki and I've got some amazing answers :D
I added placeholders for inputs and aria-labels for all components. And I've added light mode. But it's only working when light mode is switched on in OS.
I need to find a way how to toggle light-dark() function.

Well, probably there's no other way to toggle that. But i'll find the solution.
On the other hand I added few animations and improved aria-labels.