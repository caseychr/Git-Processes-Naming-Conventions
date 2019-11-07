# GitLab Processes & MR Naming

## Purpose
To quickly understand Digital Insight's Merge Request processes for more efficient and readable reviews. The priority here is clean and concise commit history for merge requests as well as traceability in JIRA.

## Rebasing 
```git rebase``` takes the commits of the current branch and appends them to another branch.
```git rebase [upstream] [current branch]```
Note: if you are on the current branch you wish to rebase running ```git rebase [upstream]``` is sufficient

Rebasing gives us the advantage of stream lining the commit history.

https://medium.com/@gabriellamedas/git-rebase-and-git-rebase-onto-a6a3f83f9cce

## Squashing
Good coding practice is to push commits early and often but this can be tedious for anyone reviewing the code. Therefore commits need to be squashed well-defined, well-labeled commits. This makes it more readable for the reviewer.

### Squashing into 1 commit
On the branch you wish to squash run ```git rebase -i``` which will open up VI for your to squash your commits. Hit `i` to edit the VI and replace `pick` with `squash` for all the commits below the top most commit; leave the top commit as `pick`. Hit `esc` and then `:wq` to save the edits to the VI. (If you wish to leave the VI without saving any of your edits hit `esc` and `:q` to cancel)

### Squashing into several commits

### Rebasing squashed commits with current branch

## Merge Request Naming Conventions and Styling

```
(title)
AND-14795: Welcome screen shell for mobile cash

(body)
This adds a new Mobile Cash screen, which for now just shows the text "Welcome". The "Welcome" text is currently just a local english string that will eventually be thrown away once we add the content for this screen in a separate upcoming ticket. MRs will probably not be as small as this in the future, but since we are ramping up in the code we decided to keep the work in jira tickets very small and focused. 
The logout button will not show until we start actually showing content (with fragments). 
I also decided to have the MVP architecture MR come through in a separate ticket to keep things focused. 
Note: this feature is guarded by a build time flag `mcw_enabled` and will be disabled until we have a complete feature ready for test. 
# Does this MR meet the acceptance criteria?
- [x] Follow [Contribution Guidelines](CONTRIBUTING.md)
- [ ] Add [CHANGELOG.md](CHANGELOG.md) entry (if appropriate)
- [ ] Create or update documentation
* Testing
    - [ ] Create or update unit tests
    - [x] Test on multiple devices
* Dependencies
    - [x] Ensure other teams (iOS, Tools, DI Labs, BMA) are in sync```
