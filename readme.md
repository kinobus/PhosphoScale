#PhosphoScale

By Nick Robin

###Changelog

-Version 0.0.0 
13 Dec 2012
Initial version

###Developer Guide

####Requirements
*	git
*	grunt

####Quick Start
1.	Set up a local development environment (make sure you have the requirements installed locally)
2.	make a local clone of the project https://github.com/kinobus/PhosphoScale.git
3.	set up git remote origin:

		$git remote origin https://github.com/kinobus/PhosphoScale.git


####Development Workflow

1.	Develop locally with grunt
  	
  		$grunt server

2.	Test and make sure whatever feature you are working on doesn't break anything, use karma to run tests (karma should run automatically at each save while running grunt watch)

3.	When you make something that works, build an optimized version of the app to the dist folder

		$grunt build

4.	To save changes to the local development environment

		$git add *
		$git commit -m "this is what i made"

5.	To save changes for the project (warning: make sure you didn't break anything first!)

		$git push origin master

6.	To deploy the dist folder in the project to github pages (might as well do this assuming you did all the right tests)

		$git subtree push --prefix dist origin gh-pages


####Deployment
We deploy to github pages, which uses a branch called gh-pages, as outlined in http://yeoman.io/deployment.html

the gh-pages branch is set up as a subtree of the root project that points to a folder called dist '/PhosphoScale/dist/'


in a bash prompt where the current working directory is the project root directory '/PhosphoScale/' type:

		$git subtree push --prefix dist origin gh-pages

This deploys the master branch