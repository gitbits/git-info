git-info and friends
====================

Synopsis
--------

* git-info - shows information about a Git repository a la `svn info'
* git-editor - invokes the editor that Git would pick
* git-pager - invokes the pager that Git would pick

How to set up
-------------

Just place these scripts in one of the directories in your `PATH`, and
you are done.

How to use
----------

	git info
	git info ~/src/somewhere/somefile
	git info some/relative/file_or_directory
	git info ~/repos/something.git

Sample output
-------------

	% git info
	Repository Path: /home/knu/src/github/git-info/.git
	Path: /home/knu/src/github/git-info
	Remote Repositories:
		origin	git@github.com:knu/git-info.git (fetch)
		origin	git@github.com:knu/git-info.git (push)
	Remote Branches:
		origin/HEAD -> origin/master
		origin/master
	Local Branches:
		* master
	Repository Configuration:
		[core]
			repositoryformatversion = 0
			filemode = true
			bare = false
			logallrefupdates = true
		[remote "origin"]
			fetch = +refs/heads/*:refs/remotes/origin/*
			url = git@github.com:knu/git-info.git
		[branch "master"]
			remote = origin
			merge = refs/heads/master
	Last Changed Commit ID: da32fa59f7fab84606ce3c144e636043e96d8063
	Last Changed Author: Akinori MUSHA <knu@idaemons.org>
	Last Changed Date: Tue Jul 28 10:37:09 2009 +0900
	Last Changed Log:
		Take the directory as a physical path.

Author
------

Copyright (c) 2009, 2012 Akinori MUSHA.

Licensed under the 2-clause BSD license.  See `LICENSE.txt` for
further details.
