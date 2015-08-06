# SVN to GIT Scripts

These scripts are to support a migration from SVN to GIT. They pull a single SVN repository with multiple modules and individual stdlayout under each module. It then combines them into a single repository based on the project file you give it.

This was made to support a Mass Migration effort

##Files:
* svnauthors.sh
* * This iterates over all the directories in the current folder and outputs all the SVN Authors to a file. It then sorts that file so only Uniques are left. You must edit the file to put in the correct email for people (or don't if you like them wrong).
* svnupgrade.sh
* * This iterates over all the directories in the current folder and runs the svn upgrade command. This was made because some SVN's I operated on were pretty old and it's important to move them up (locally) so the authors script can run properly.
* stgandcombine.sh
* * Heart and soul, this clones the repo from SVN, moves all files to a subfolder (same name as the module) and all successfully migrated repo's are then combined into 1 GIT repo.
* * All traces of the previous link to SVN are removed... THIS IS ONE WAY ONLY (why would you want to go back?).
* * depends on 2 files, the config.properties and your project list, also has 1 input of what you want the combined GIT repository to be named.

##Layouts supported:
servername/reponame/modulename/stdlayout
```
ProjectA
   trunk
   branches
   tags
ProjectB
   trunk
   branches
   tags
```
#Links:
http://svnbook.red-bean.com/nightly/en/svn.reposadmin.planning.html#svn.reposadmin.projects.chooselayout
