git-ls-branches
===============

Synopsis
--------

* git-ls-branches - lists branches sorted by date

Usage
-----

    git ls-branches [options]

        -v, --verbose         be verbose
        --color               turn on color even if stdout is not a tty
        --no-pager            do not pipe output into a pager

        -a, --all             list both remote-tracking and local branches
        -r, --remotes         list remote-tracking branches
        --no-merged=<commit>  print only not merged branches
        --merged=<commit>     print only merged branches
        -t[dDirt]             specify time format (cf. %c[dDirt])

Example
-------

    % git ls-branches
    * master                                         (2 weeks ago)
      m17n                                           (1 year, 6 months ago)
      1.4                                            (1 year, 7 months ago)
      encoding_fix                                   (1 year, 7 months ago)
      http_equiv_headers                             (2 years, 1 month ago)

    % git ls-branches -ti --verbose
    * master                                         (2013-01-19 22:31:25 -0500) 9af8b10 add more changes to the changelog. 
      m17n                                           (2011-08-18 21:58:07 +0900) 11df7c9 Add a failing test that should be passing. 
      1.4                                            (2011-07-01 00:53:44 -0400) 66b46cf Release prep: bumping version to 1.4.7 and updating the changelogs. 
      encoding_fix                                   (2011-06-30 12:09:51 +0900) db14750 Add support for <meta charset="..">. 
      http_equiv_headers                             (2011-01-16 23:46:27 +0900) f4cfa15 Add HTML#http_equiv_headers. 

Actual output will be nicely colored, and also automatically
pagerized just like other git commands.

Description
-----------

`git-ls-branches(1)` requires `git-pager(1)` for invoking a pager.
Get it from <https://github.com/gitbits/git-info>.

License
-------

	Copyright (c) 2013 Akinori MUSHA

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
