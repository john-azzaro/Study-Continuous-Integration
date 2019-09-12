# Continuous Integration (CI) Study
* [What is the Continuous Integration Study?](#What-is-the-Continuous-Integration-Study)
* [What is Continuous Integration (CI)?](#What-is-Continuous-Integration-(CI))
* [What is Travis CI?](#What-is-Travis-CI)
* [How do you use Travis CI?](#How-do-you-use-Travis-CI)
* [What is Travis CLI?](#What-is-Travis-CLI)

<br>

## What is the Continuous Integration Study?
The continuous integration study is an examination of best practices associated with CI, where you essentially work with a main shared repository that is continually updated.  Addiitonally, this study examines tools such as Travis.CI to use 
in the development workflow.

<br>

## What is Continuous Integration (CI)?
**Continuous Integration**, or CI, is a development practice where developers integrate working copies of code to a central shared repository several times a day.  When each integration is submitted to this shared repository, it is verified by an automatic build.

CI is envaluable to developers in that it can:
1. *Solve problems quickly by detecting and locating errors.*
2. *Spend more time building features instead of fixing problems.* 
3. *Help developers frequently integrate code often to communictae betwene engineers and get feedback.* 
4. *Make sure code is consistent.*
5. *Help make code much more dependable with automated testing.* 
6. *Make sure the code each dev is working on does not deviate too far from the a common plan of action.*
7. *Verify each integration via autmated build and automated tests.*
8. *Can integrate with tools like slack, email, etc.*
 
<br>

## What is Travis CI?
Travis CI is a free hosted continuous integration platform that is used to build and test open source project hosted on github.  With the service, you can signup, 
link to a repository, build, and test apps.  Although there are other CI tools, such as Jenkins (which will be covered in a future study), Travis CI is very easy to use 
in conjunction with a Github account.

| **Description:**                            | **Link:**                             |
| ---------------------------------------- | ----------------------------------------------|
|  Travis-ci.org               |  https://travis-ci.org/getting_started             |
|  Travis CI documentation               |  https://docs.travis-ci.com             |
|  Travis CI Github              |  https://github.com/travis-ci/travis.rb            |


<br>

## How do you use Travis CI?

### STEP 0: Sign-up/Sign-in for Travis CI
Note that you can sign-in using your Github account.
```
    https://travis-ci.org/getting_started
```

### STEP 1: Select your repository and turn ON
In your Travis.ci account, select the respository listed from your Github account.  There will be a switch next to the respository that you can turn on and off.
Turn the respository on.
```
    travis-ci.org/account/respositories   ==>  Turn ON
```

### STEP 2: Create a .travis.yml file
In your root project file, create a ".travis.yml" file.  This will allow you to tell Travis CI what to do.  
``` 
    .travis.yml 
```

### STEP 3: Inside your .travis.yml file, tell Travis CI what to do
In the code below, we are doing two thing in the two lines code.  First, we are telling Travis CI to treat the project as a node project.  Second, ``` node_js: node ``` tells Travis CI to use the latest stable release for the test enviroment.
```JavaScript
    language: node_js
    node_js: node
```

### STEP 4: Commit the .travis.yml file to version control
When you eventually push the file to your existing repository (and assuming you have turned the corresponding repository on Travis CI to "on"), this will automatically trigger a *build* on Travis CI.  When you go to your project on travis-ci.org, you will either be running or waiting to run your test suite.
```
git add .
git commit -m 'added ci file'
git push origin master
```

<br>

## What is Travis CLI?
Travis CLI will allow use to work with Heroku and allow you to run test automatically when you push changes to your master repository or merge a pull request into the master.  The
way we have the following setup, TravisCI will deploy to Heroku if the tests pass.  If they do not, they will not deploy.

<br>

## How do you use Travis CLI?

### STEP 0: Install Travis CI command line interface
To do this, you may need to install Rudy on your computer if you use windows because it does not come insalled on your machine.  To do this, simply visit the ruby website. You may or may not have Ruby installed, so check first to see if you have it.  Then in Gitbash install Ruby.  Note that when you install ruby in gitbash, you use the prfix "gem", which is the Ruby equivalent of NPM.
```
    ruby -v          // check for version of ruby installed
```
```
    gem install travis
```

### STEP 1: Using command line, in your project file login to travis
Log into Travis with your Github credentials.  Please note that it would be better to use command prompt instead of Gitbash for the remaining steps to avoid any errors.
```
    travis login
```

### STEP 2: Setup Travis to deploy to Heroku
When you run this command in Gitbash, you will be prompted through a series of defaults.  Just hit enter for each of these as the defaults are good for a standard project.
```
    travis setup heorku
```

### STEP 3: 




