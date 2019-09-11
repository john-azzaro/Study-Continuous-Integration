# Greensock Animation API Study


## Study Contents:

* [What is the Continuous Integration Study?](#)
* [What is Continuous Integration (CI)?](#)
* [What is Travis CI?](#)
* [How do you use Travis CI?](#)

<br>

## What is the Continuous Integration Study?
The continuous integration study is an examination of best practices associated with CI, as well as the use tools such as Travis.CI to use 
in development workflow.

<br>

## What is Continuous Integration (CI)?
**Continuous Integration**, or CI, is a development practice where developers integrate working copies of code to a central shared repository several
times a day.  When each integration is submitted to this shared repository, it is verified by an automatic build.

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

<br>

## How do you use Travis CI?

### STEP 0: Sign-up/Sign-in for Travis CI
Note that you can sign-in using your Github account.

### STEP 1: Select your repository and turn ON
In ```travis-ci.org/account/respositories```, select the respository listed from your Github account.  There will be a switch next to the respository that you can turn on and off.
Turn the respository on.

### STEP 2: In your root project folder, create a ".travis.yml" file
Simply create a ``` .travis.yml ``` file.

### STEP 3: Inside your .travis.yml file, insert code
Inside the file, insert the following code:
```JavaScript
    language: node_js
    node_js: node
```
When you insert the code above, it tells Travis CI to treat the project as a node project.
For example, ``` node_js: node ``` tells Travis CI to use the latest stable release for the test enviroment.

### STEP 4: Commit the .travis.yml file to version control
When you eventually push the file to your existing repository (and assuming you have turned the corresponding repository on Travis CI to "on"), this will automatically
trigger a *build* on Travis CI.




