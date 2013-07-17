SVN 2 Git
=========

Purpose
-------

Automate versioning from SVN to Git. For lazy people.

This script may be useful if you use SVN to share code but use git locally to version your files. This small script is not related at all to git-svn. It may prove useful when SVN and Git are used independently.

When doing `svn up`, if files versionned by Git are deleted, we have to manually remove them for the Git repo. This script tries to automate the process.

And it's also the occasion to learn basic BASH programming.

How it works
------------

1. Update the SVN repo
2. Add files with `git add .`
3. Remove files deleted by SVN
4. Commit with a predefined commit message "SVN Update, revision XXX". XXX is automatically inserted.

You can customize the commit message if you want.


Usage
-----

1. Copy the script somewhere in your $PATH, like /usr/bin

`sudo cp svn2git /usr/bin` // sudo required for /usr/bin, YMMV

2. Give execute permission to everyone

`chmod a+x /usr/bin/svn2git` // adapt path and permissions according to your wishes

3. Ready to go ! Just type `svn2git`.



License
-------

The MIT License (MIT)

Copyright (c) 2013 Khalid Jebbari

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of
the Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
