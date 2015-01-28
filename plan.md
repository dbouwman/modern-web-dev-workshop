# Modern Web Development Workshop

8:30-5:30
Hilton

### DESCRIPTION
Fullday workshop that covers the core tools and practices of modern front-end web development. Regardless of the javascript framework or editor you use, leveraging automation to ensure fast, consistent front-end workflows is massive productivity booster. Led by 3 Esri front-end developers who utilise these tools on a daily basis to ship web apps used by thousands of organizations.

### WHAT DO I NEED TO BRING?
Students must bring a laptop containing a recent version of Windows, Mac OSX, or Linux. You should install nodejs, Chrome, have a github account and github tooling on your machine (commandline or GUI). Unfortunately for this course, loaner or classroom machines are NOT provided or available. You must bring your own.


### WHY DO I NEED THIS CLASS?
Modern web applications utlize many technologies. At the core are HTML, Javascript, CSS, but that is only the beginning. In this workshop we will discuss how to optimize both the code you create, and the workflows use to create it. By the end of the day you will be able to go from an empty folder to a live application in under 5 mintes. What's more that application will be a great starting point for your real-world projects as it will have all the tooling and automation required to develop, build and deploy a modern web application.

### PREREQUISITES
This course assumes you have solid experience with JavaScript, HTML and CSS. We also assume you have a github account, and are familliar with the basic git commands like clone, push, pull.


## Intro: What do we mean by "Modern Web Dev"
- Native Web Apps (Heinrik)
- responsive (or not) sites
- lots of js interactions
- possibly a spa or hybrid
- Developer Expectations: low-friction workflow, instant feedback, one command deploy. Focus on solving problems not tools/fighting w/ env, deploy etc
- End-User Expectations: page load speed / 1000ms to glass

## Modern Workflow: 101
- git is life (working in branch, merge to master etc)
- package management - npm & bower - keeping deps up to date, easy to add
- allows devs to pull, install, and be running very quickly
- automate all the things
- gulp, grunt, npm, batch/sh
- live-reload (multi-device, multi-browser)

### Hand-On #1 gulp-webapp  (Jupe)
- npm install -g yo
- npm install -g generator-gulp-webapp
- mkdir demo1 && cd demo1
- yo gulp-webapp
	- NO to SASS??? 
#### WINDOWS:
- if issues w/ ruby-sass:
	- npm uninstall --save-dev gulp-ruby-sass
	- npm install --save-dev gulp-sass
	- gulpfile.js
	- var gulpSass = require('gulp-sass');
	- change rubySass --> gulpSass

- DEMO: live-reload

## Modern Workflow: Power Tools
- linting
- unit tests
- pre-compile templates (jst/etc)
- css pre-procssors (Patrick Arlt)


### Hands-on #2 open-data-starter
- fork @ github
- clone locally
- gulp serve
- Note how fast / easy that was (assuming internet holds!)

##### Sass Changes w Live Reload (Patrick Leading)
- git checkout -b sass-edits
- edit the sass vars file and see updates
- add new page-specific nested rules
- checkout master
- git merge sass-edits

##### Linting (Jupe)
- change js to add a lint error
- see error in terminal

##### Unit Tests (Jupe)
- make change that breaks tests
- see tests fail, edit back to happiness

##### JST (Jupe)
- change template
- see refresh


# LUNCH FOR THE PEOPLES


## Build Process
- why build?
- ref page-load speed
- what is a front-end build? 
- combine & min css, js, html
- UseMin & MinifyCSS
- image optimization
- cache busting (rev)
- Optimizations: Above the Fold CSS, server-side-rendering etc
- show webpagetest.org & some open-data results
- should build artifacts be checked in? No

### Hands-on #3 Compile and Serve
keep working with open-data-starter

##### Working Build  (Jupe)
- add js/css/html build step step (have this in a gist)

##### Testing Locally  (Jupe)
- create a serve:dist task
- make sure that build runs on changes!



## Deployment
- general process
	- move ./dist to ???
- gh-pages
- s3
- other (ftp, file share, zip + majicks) 

### Hands on #4  (Jupe)
- add gulp-gh-pages
- add status.json task (so app knows it version)
- run!
- beer.




