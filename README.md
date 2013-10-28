git-flow-feature-arc
====================

**ATTENTION:** Following some comments from https://github.com/lonetwin I decided to add my modifications on a fork of the original source code <https://github.com/nvie/gitflow>. This way the installation process will be more straight forward for future users. You can find the forked version here <https://github.com/bogdanmic/gitflow>

This is the git-flow-feature file from <https://github.com/nvie/gitflow> with a few modifications to use "arc diff" and "arc amend" to open and close review requests.
All the credits for building git-flow belong to its original owner.

To use this file, rewrite the original file from <https://github.com/nvie/gitflow> named **git-flow-feature** with this one and install gitflow as usual.

**NOTE:** Use this file at your own risk. It is very likely that it will not be maintained with any bugfixes ore modifications that apprea in the future to the original file.


#### What is so special about this file?

Well first for it to work you need to have installed this <https://github.com/facebook/arcanist> installed.
This is a component used by [phabricator](http://phabricator.org/) to do code review.

For more details on installing **Phabricator** please check their documentation <http://www.phabricator.com/docs/phabricator/article/Installation_Guide.html>

After you do that, this file allows you to:
 
 - create a code review request to the phabricator server
 			
 		git flow feature review   # it executes "arc diff develop"
 - close the review requests after they are accepted
 
 		git flow feature finish   # it executes "arc amend" at the beginning of the normal process
 		
#### How does this file modify my flow?
The new flow for a feature looks something like this:

	git flow feature
	git flow feature start <name> [<base>]
	git flow feature review
	git flow feature finish <name>
 		

I hope this is clear enough. If not, ask and maybe i will listen :)

#### Works on
It works on mac and other linux based systems.
Don't know about widows though.