# githubworflow 

### Clone your fork and map only the Matrix branch to the upstream Matrix branch
git clone https://github.com/phunkfish/pvr.mediaportal.tvserver
git remote add upstream https://github.com/kodi-pvr/pvr.mediaportal.tvserver
git fetch upstream
git branch -u upstream/Matrix Matrix

### Create a new dev branch but update to latest upstream first
git checkout Matrix
git pull
git checkout -b my-dev-branch

### Rebase dev branch to latest version from upstream
git checkout Matrix
git pull
git checkout my-dev-branch
git rebase Matrix

Push dev branch to your fork
git push origin my-dev-branch

Force push dev branch to your fork
git push origin -ff my-dev-branch

## Make changes

git add -u
git commit —amend

### Then force push it with:

git push origin -ff your-branch-name

