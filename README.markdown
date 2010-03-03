git-info and friends
====================

Synopsis
--------

* git-info - shows information about a Git repository a la `svn info'
* git-editor - invokes the editor that Git would pick
* git-pager - invokes the pager that Git would pick

How to set up
-------------

Assuming you are installing these scripts in ~/bin, run the following
commands:

	install -m 755 git-pager ~/bin/
	install -m 755 git-info ~/bin/
	git config --global alias.pager '!$HOME/bin/git-pager'
	git config --global alias.info '!$HOME/bin/git-info'

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
	
License
-------

	Copyright (c) 2009 Akinori MUSHA
	
	All rights reserved.
	
	Redistribution and use in source and binary forms, with or without
	modification, are permitted provided that the following conditions
	are met:
	1. Redistributions of source code must retain the above copyright
	   notice, this list of conditions and the following disclaimer.
	2. Redistributions in binary form must reproduce the above copyright
	   notice, this list of conditions and the following disclaimer in the
	   documentation and/or other materials provided with the distribution.
	
	THIS SOFTWARE IS PROVIDED BY THE AUTHOR AND CONTRIBUTORS ``AS IS'' AND
	ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE
	IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE
	ARE DISCLAIMED.  IN NO EVENT SHALL THE AUTHOR OR CONTRIBUTORS BE LIABLE
	FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL
	DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS
	OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION)
	HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT
	LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY
	OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF
	SUCH DAMAGE.
