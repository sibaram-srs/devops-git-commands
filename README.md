# Git + DevOps Basic Commands Cheat Sheet (with idea)

# Git is a version control system used to track code changes, collaborate, and manage deployments in DevOps pipelines.

```bash

git --version                            # check git installed version
git config --global user.name "Name"     # set your identity
git config --global user.email "email"   # set email for commits

git init                          # initialize git repo in project
git clone <repo-url>              # copy remote repo to local machine

git status                        # shows modified/untracked files
git log                           # commit history
git diff                          # changes not yet staged
git show                          # details of a commit

git add .                         # add all changes to staging
git add <file>                    # add specific file

git commit -m "msg"               # save snapshot of changes
git commit -am "msg"              # add + commit tracked files

git branch                        # list branches
git branch <name>                 # create new branch
git checkout <name>               # switch branch
git checkout -b <name>            # create + switch branch
git switch <name>                 # modern way to switch branch
git switch -c <name>              # create + switch branch

git merge <branch>                # merge branch into current branch
git rebase <branch>               # rewrite commit history (advanced)

git remote -v                     # show remote repo links
git remote add origin <url>      # connect local repo to GitHub

git push origin main             # send code to GitHub
git push -u origin main          # set upstream tracking
git push                         # push changes
git push --all                   # push all branches

git pull                         # fetch + merge latest changes
git fetch                        # only download changes

git stash                        # temporarily save work
git stash list                   # list stashed work
git stash pop                    # restore latest stash

git reset --soft HEAD~1         # undo commit but keep changes
git reset --hard HEAD~1         # remove commit + changes (danger)
git revert <commit-id>          # safely undo commit

git tag                         # list tags (versions/releases)
git tag <name>                  # create version tag
git push origin <tag-name>      # push tag to remote

git cherry-pick <commit-id>     # apply specific commit

git log --oneline --graph --all # visual commit tree

git clean -fd                   # remove untracked files

# IDEA (DevOps context):
# Git is used in DevOps pipelines (CI/CD) where code is:
# Developer -> GitHub -> Jenkins/GitHub Actions -> Build -> Test -> Deploy (Docker/K8s)
# Every commit can trigger automated deployment.
