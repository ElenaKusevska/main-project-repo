this repository illustrates the easiest way to add one subproject from it's git repo as a subdirectory to another main project, preserving both commit histories.

### Here is the list of git/bash commands I used for this:

Clone both directories
```
git clone git@github.com:ElenaKusevska/main-project-repo.git
git clone git@github.com:ElenaKusevska/subproject-repo.git
```

Create subproject directory in subproject-repo
```
cd subproject-repo
mkdir subproject
mv * subporoject
```

Go to main project and add the remote branch of subproject.
Pull subproject and merge with main project
```
git remote add subproject-clone git@github.com:ElenaKusevska/subproject-repo.git
git pull subproject-clone main --allow-unrelated-histories
git push
```
 
