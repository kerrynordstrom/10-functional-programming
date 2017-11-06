![CF](https://camo.githubusercontent.com/70edab54bba80edb7493cad3135e9606781cbb6b/687474703a2f2f692e696d6775722e636f6d2f377635415363382e706e67) Lab 10: Functional Programming
===

## Submission Instructions
Follow the submission instructions from Lab 01.

## Resources  


[MDN: map()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map)

[MDN: filter()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)

[MDN: reduce()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce)

## Configuration
_Your repository must include:_

```
10-functional-programming
├── .eslintrc.json
├── .gitignore
├── LICENSE
├── README.md
├── node_modules
├── package-lock.json
├── package.json
├── public
│   ├── data
│   │   └── hackerIpsum.json
│   ├── admin.html
│   ├── index.html
│   ├── new.html
│   ├── scripts
│   │   ├── article.js
│   │   └── articleView.js
│   ├── styles
│   │   ├── base.css
│   │   ├── fonts
│   │   │   ├── icomoon.eot
│   │   │   ├── icomoon.svg
│   │   │   ├── icomoon.ttf
│   │   │   └── icomoon.woff
│   │   ├── icons.css
│   │   ├── layout.css
│   │   └── modules.css
│   └── vendor
│       └── styles
│           ├── default.css
│           ├── normalize.css
│           └── railscasts.css
└── server.js
```

## Feature Tasks

*As a user, I want an admin page so I can easily view the stats of my blog app.*

- For both index.html and admin.html, we'll want access to the `Article.all` data... but we'll have different view functions to set up for each of those pages. Complete the `Article.fetchAll()` method so that it calls a `next` parameter: a function to invoke when its work is done.  

*As a developer, I want to utilize IIFEs so that all of my function calls are executed on page load.*

- Let's make sure each one of our scripts are properly enclosed. Wrap the contents of article.js and articleView.js in an IIFE, like we did in class. Then pass in the new "app" object as an argument to the IIFEs and be sure to remember to export the `Article` and `articleView` objects. Keep in mind that this will change how we refer to those two objects throughout the app.
- Ensure both the index page and the admin page call `Article.fetchAll()` in a way that properly triggers the appropriate page setup methods.

*As a developer, I want to utilize functional programming so that my code makes sense and follows modern practices.*

-  Use the array methods `.filter()`, `.map()`, `.reduce()`, and `.forEach()` to transform the data into what you need it to be. Chain these methods together as needed.

### Stretch Goal

*As a user, I want additional stats so that I can track the progress of my app.*

- What additional statistical analysis would be of interest to you with this data set? Code it up!

## Documentation
_Your README.md must include:_

```md
# Project Name

**Author**: Kerry Nordstrom
**Version**: 1.0.0 (increment the patch/fix version number up if you make more commits past your first submission)

## Overview
<!-- This application now includes functionality to take in new article submissions, display all articles organized by date written, calculate and display total articles, total words, and words by author.  It will also dynamically update with any new authors and their totals. -->

## Getting Started
<!-- The user must fork and clone the repo for 10-functional-programming from codefellows-seattle-301d25 to their local machine.  They must also configure and link PostgreSQL and open node.js on port 3000.   -->

## Architecture
<!-- Provide a detailed description of the application design. What technologies (languages, libraries, etc) you're using, and any other relevant design information. -->

## Change Log
<!-- Use this are to document the iterative changes made to your application as each feature is successfully implemented. Use time stamps. Here's an examples:

11-05-17 12:05pm - Wrapped logic in article.js and articleView.js in IIFE, set conString value to link postgreSQL to project.  Opened node server at port 3000.

11-05-17 1:30pm - Called methods on all HTML pages, making sure to use app. notation which makes pages outside of the IIFE able to access methods that are now attached to app.Article

11-05-17 10:00pm - Finalized all .map().reduce() logic totaling all words and filtering these totals to individual authors.

11-06-17 10:00am - Corrected Handlebars template and inserted callback function to the .fetchAll method on admin.html

11-06-17 10:15am - Corrected Article constructor to include app. notation which allows it to attache to app.Article and correctly instantiate a new object article on the new.html page.

## Credits and Collaborations
<!-- Give credit (and a link) to other people or resources that helped you build this application. -->
-->
```
