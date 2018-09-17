# Pretested through the CLI

## As a developer

### fetch and deliver changes

* Change branch to the branch you would like to push changes to afterwards: `git checkout master`

* Make sure that you are working on the latest changes from the server: `git pull --rebase`

* Make a new branch to work with: `git checkout -B DEV-321-something --track origin/master`

* Work

* Stage your work: `git add {files}` to stage some files, or `git add .` to stage all

* Commit your work with a message: `git commit -m "#321 added new test case"`

* Make sure that you are building your code on the latest master: `git pull --rebase`

* Ensure that there are no conflicts

* Push your changes for integration: `git push origin DEV-321-something :ready/ DEV-321-something`

### Integration failed

* checkout your failed branch: `git checkout DEV-321-something`

* Replay your work on top of master to get the issues/conflicts: `git pull --rebase`

* Fix the problem - solve the merge conflicts

* continue with the rebase of code: `git rebase --continue`

* Delete the old pushed branch: `git push origin --delete ready/DEV-321-something`

* Push the local branch with the resolved merge conflicts: `git push origin ready/DEV-321-something`

### One commit push

* To view how many commits your are committing to master `git log --oneline --decorate --graph master HEAD`

* Interactive rebasing your commits on top of master: `git rebase -i master DEV-321-something`

* Push your local branch: `git push origin ready/DEV-321-something`

### Clean up

* Clean up all local merged branches `git fetch [ --all --prune ]`
