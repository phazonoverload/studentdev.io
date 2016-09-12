# StudentDev

A curated list to help you become a great student developer.

## One-time Setup 

### Prerequisites

* [Node.js](https://nodejs.org/en/).
* [Roots](http://roots.cx/) `npm install roots -g`.

## Quick Start

### Getting this site running locally

1. `git clone` this repo down and `cd` into the folder from a terminal.
2. Run `npm install`.
3. Run `roots watch`.
4. Make changes.
5. To stop the local web server, just hit ctrl + c. 

## Deploying

1. Install [Ship](https://github.com/carrot/ship) `npm install ship -g`
2. Manually add a CNAME file in the /public folder - it should contain one line: `studentdev.io`
3. `cd` to the project directory
4. `ship public -to gh-pages`
5. Enter your credentials - the file these are stored in is already included in .gitignore

## A guide to the file structure

### Views (/views)

Views describe the pages which users see and interact with. Here's the noteworthy top-level points: 

* These are written in a preprocessor called [Jade](http://jade-lang.com/) (soon to be called Pug).
* This uses indentation to describe nested tags.
* Currently there is only one template in this site - index.jade.

### Styles (/assets/css)

* These are written in a preprocessor called [Stylus](stylus-lang.com).
* The main file is master.styl, which in turn imports the rest of the files.
* To change the blue accent color, change `$color` on line 2.
* To change the breakpoint to swap to mobile view, change `$breakpoint` on line 1.
* If you want to change the site-wide font, change the font-family name in line 10 of _base.styl (remember to include a reference to it in views/layout.jade).

### Images (/assets/img) 

* Just drop the images in this directory for them to be accessible from /img/FILENAME in the views. 

## Adding new content

/views/index.jade is fairly self-explanatory. It's written in Markdown. 

1. Start the local server with `roots watch`
2. Add your content using [Markdown](https://daringfireball.net/projects/markdown/) indented inside of the `:marked` section
3. If you want to add new sections, add a new `h1` element and a new Markdown section below it
