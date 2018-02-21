
This repository is designed to serve as a template for hosting your plugins in a plugin library.  Plugins placed in the plugin 
folder will be hosted on the github pages site for this repository automatically, and commits to the `master` branch will 
automatically update the library.  This README assumes familiarity with git and github.


## Setup:

* Setup a github.com account if you do not have one.  

* Fork this repository to your own github account.  

* In `gui/Library.tid` replace `{GITHUB PAGES URL}` with the github pages url where you're planning to host this.  Typically, 
this is of the form `{github username}.github.io/{repo name}.`  So for example, if my repository was available at 
`https://github.com/mklauber/tw5-plugins` I would replace `{GITHUB PAGES URL}` with `mklauber.github.io/tw5-plugins`.  
Commit and push this code to github.com

* Sign into travis-ci.org with your github credentials.  

* Enable builds for your forked repository.

* Generate a github token, ala https://help.github.com/articles/creating-a-personal-access-token-for-the-command-line/ to 
allows travis-ci to upload to your github pages.  You'll need to have repo scope on this token.  

* Go to settings for your travis-ci job and add an environment variable with the name `GITHUB_TOKEN` and the set the value to 
the github token string from the previous step.

* At this point, travis should attempt to build and publish your plugins.  If all goes well, check your library at 
`{github username}.github.io/{repo name}.`


