![rug](http://www.internetrugs.com/blog/wp-content/uploads/2008/06/india-zamin-oriental-rug.jpg)

Grunt Ember Boilerplate
=======================

This is a [Grunt.js](http://gruntjs.com/) `0.4x` starter project that
gives you everything you need to start developing
[Ember.js](http://emberjs.com) applications.

You get:  
- Handlebars precompilation
- Ember Idiomatic integration tests with Qunit
- Base folder setup
- Commonjs modules
- Coffeescript
- Stylus for CSS
- Normalize.css for the best browser reset
- A precompilation directive for production deploy
- Live reload for even better local development

Why?
====
Literally so many projects that do this kind of stuff.  
- Yeoman, uses Grunt.js, awesome! Lacks coffeescript and commonjs
modules
- Brunch.io does not use Grunt.js (Grunt.js is a really great task
runner with a very vibrant community / contrib library)
- Ember-tools, I love this project and use it within grunt on other
projects... but it doesn't have coffeescript and it's not as flexible as
a grunt project.

This project is just boilerplate Grunt.js, modify the `Gruntfile.coffee` to
do whatever you want, you have the entire Grunt.js ecosystem!! I've
actually used this project in replacement of the Rails asset pipeline,
so you can use the output files within whatever project you have
currently... throw away the `index.html` file, modify `Gruntfile.coffee`
to output the files wherever you need.

Instructions
============

1. Install the Grunt CLI globally  
`npm install -g grunt-cli`

2. Clone the repo with your own directory name and remove prior `.git`
folder  
`git clone https://github.com/lsdafjklsd/grunt-ember-boilerplate.git
your-application-name`  
`cd your-application-name && rm -rf .git`

3. Install project dependencies  
`npm install`

Now to develop your application, run the `grunt watch` command. This
will run the default action (which does everything) anytime a file in
`libs/` changes. It will also watch Javascript files in the integration
folder and run the tests when a file is changed.

When you want to deploy, run the `grunt precompile` command to generate
a production ready version of the `js/application.js` file.

If you're using the `public/index.html` in production, be sure to delete the live-reload script tag at the bottom of the page.

Develop in the `libs` directory, your generated files end up in the the
`js` and `css` folders in the public directory.

For an idea on how to incorporate Ember Data, check out my on-going
Forum project [here](https://github.com/lsdafjklsd/vmware-frontend/tree/master/forum/js)

If you are new to Ember, and are not sure how to set up a project, check
out Ryan Florence's
[Ember-tools](https://github.com/rpflorence/ember-tools) That project
provides rails-like-scaffolding, and this project's file structure is based
on that.

Testing
=======

Testing is really easy in Ember, if you have done integration tests in
other environments this will be a breath of fresh air. If you are new to
testing, integration tests are a great way to ease into testing because
it allows you to automate the clicks and steps you would normally manually go through.
Sample tests are provided in this project which give you basic `navigate
here, look for this content`. There are more helpers available to you
and I suggest you watch this [lightning
talk](http://www.youtube.com/watch?v=nO1hxT9GBTs&feature=youtu.be) by Erik Bryn on the
subject.  


Todos
=====

1. Make this an actual grunt project template, versus cloning this
   repo and deleting the existing `.git` directory.
