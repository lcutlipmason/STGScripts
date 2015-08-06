# SVN to GIT Scripts

These scripts are to support a migration from SVN to GIT. They pull a single SVN repository with multiple modules and individual stdlayout under each module. It then combines them into a single repository based on the project file you give it.

This was made to support a Mass Migration effort

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
