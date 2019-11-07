# GitLab Processes & MR Naming

## Purpose
To quickly understand Digital Insight's Merge Request processes for more efficient and readable reviews. The priority here is clean and concise commit history for merge requests as well as traceability in JIRA.

## Rebasing
(If you need to squash your commits skip this section as it is redundant)
```git rebase``` takes the commits of the current branch and appends them to another branch.
```git rebase [upstream] [current branch]```
Note: if you are on the current branch you wish to rebase running ```git rebase [upstream]``` is sufficient

Rebasing gives us the advantage of stream lining the commit history.

https://medium.com/@gabriellamedas/git-rebase-and-git-rebase-onto-a6a3f83f9cce

## Squashing

### Squashing into 1 commit

### Squashing into several commits

### Rebasing squashed commits with current branch

## Merge Request Naming Conventions and Styling

