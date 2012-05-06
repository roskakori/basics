Git Basics
==========

This is a collection of notes on common but somewhat elaborate tasks with git.


Merge a fork with the original repository
-----------------------------------------

Source: http://bradlyfeeley.com/2008/09/03/update-a-github-fork-from-the-original-repo/

When doing this on a repository for the first time, activate tracking for the
original::

  cd ~/workspace/pep8
  git remote add --track master jcrocholl https://github.com/jcrocholl/pep8.git
  git remote

Each time you want to update::

  cd ~/workspace/pep8
  git fetch jcrocholl
  git merge jcrocholl/master

If the merge causes conflicts::

  cd ~/workspace/pep8
  git mergetool


Convert local Subversion repository to git
------------------------------------------

Example (replace "me" by user name)::

  svn2git file:///Users/me/Repositories/envSOF --tags tags --trunk trunk --nobranches

To push trunk and tags::

  git push
  git push --tags


Check out Github repository using Subversion
--------------------------------------------

Example::

  svn checkout https://github.com/roskakori/cutplace/trunk cutplace
