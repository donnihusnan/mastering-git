# Git Branch Operations Mastery Checklist

A focused guide to master all Git branch operations including creation, navigation, saving work, and merging strategies.

## 🌱 Branch Basics

### Understanding Branches
- [ ] Understand what a branch is (pointer to a commit)
- [ ] Learn the difference between local and remote branches
- [ ] Understand HEAD and what it points to
- [ ] Know the default branch (main/master) concept
- [ ] Understand branch vs commit relationship

### Viewing Branches
- [ ] List local branches (`git branch`)
- [ ] List all branches including remote (`git branch -a`)
- [ ] List remote branches only (`git branch -r`)
- [ ] Show current branch (`git branch --show-current`)
- [ ] View branch with last commit info (`git branch -v`)
- [ ] Show merged branches (`git branch --merged`)
- [ ] Show unmerged branches (`git branch --no-merged`)

## 🔄 Branch Creation & Navigation

### Creating Branches
- [ ] Create new branch from current commit (`git branch <name>`)
- [ ] Create branch from specific commit (`git branch <name> <commit>`)
- [ ] Create branch from another branch (`git branch <new> <existing>`)
- [ ] Create branch from tag (`git branch <name> <tag>`)
- [ ] Create branch and switch to it (`git checkout -b <name>`)
- [ ] Create branch and switch using switch command (`git switch -c <name>`)

### Moving Between Branches
- [ ] Switch to existing branch (`git checkout <branch>`)
- [ ] Switch to branch using switch command (`git switch <branch>`)
- [ ] Switch to previous branch (`git checkout -` or `git switch -`)
- [ ] Switch to remote branch (`git checkout -b <local> origin/<remote>`)
- [ ] Switch and create tracking branch (`git checkout --track origin/<branch>`)

### Branch Navigation Shortcuts
- [ ] Use tab completion for branch names
- [ ] Switch using partial branch names
- [ ] Navigate branch history with reflog
- [ ] Use aliases for common branch operations

## 💾 Saving Work & Save Points

### Stashing Work
- [ ] Save current work (`git stash`)
- [ ] Save with descriptive message (`git stash push -m "message"`)
- [ ] Stash including untracked files (`git stash -u`)
- [ ] Stash including ignored files (`git stash -a`)
- [ ] Stash only specific files (`git stash push <file>`)
- [ ] Create named stash (`git stash push -m "feature-work"`)

### Managing Stashes
- [ ] List all stashes (`git stash list`)
- [ ] Show stash contents (`git stash show`)
- [ ] Show stash diff (`git stash show -p`)
- [ ] Apply latest stash (`git stash apply`)
- [ ] Apply specific stash (`git stash apply stash@{n}`)
- [ ] Pop stash (apply and remove) (`git stash pop`)
- [ ] Drop stash without applying (`git stash drop`)
- [ ] Clear all stashes (`git stash clear`)

### Creating Branches from Stashes
- [ ] Create branch from stash (`git stash branch <name>`)
- [ ] Create branch from specific stash (`git stash branch <name> stash@{n}`)
- [ ] Apply stash to different branch
- [ ] Move stashed work between branches

### Commit-Based Save Points
- [ ] Create temporary commits as save points
- [ ] Use meaningful commit messages for save points
- [ ] Create commits with `--fixup` for later squashing
- [ ] Tag important save points (`git tag save-point-1`)

## 🔀 Branch Merging Strategies

### Fast-Forward Merges
- [ ] Perform fast-forward merge (`git merge <branch>`)
- [ ] Understand when fast-forward is possible
- [ ] Force fast-forward only (`git merge --ff-only`)
- [ ] Prevent fast-forward (`git merge --no-ff`)

### Three-Way Merges
- [ ] Perform three-way merge (`git merge <branch>`)
- [ ] Create merge commit with custom message (`git merge -m "message"`)
- [ ] Understand merge commit structure (two parents)
- [ ] Review merge commit in history

### Squash Merging
- [ ] Squash merge branches (`git merge --squash <branch>`)
- [ ] Understand when to use squash merges
- [ ] Complete squash merge with commit
- [ ] Compare squash vs regular merge outcomes

### Advanced Merge Options
- [ ] Merge with strategy (`git merge -s recursive`)
- [ ] Merge with strategy options (`git merge -X theirs`)
- [ ] Use patience algorithm (`git merge -X patience`)
- [ ] Ignore whitespace changes (`git merge -X ignore-space-change`)

## ⚔️ Handling Merge Conflicts

### Conflict Resolution
- [ ] Identify merge conflicts (`git status`)
- [ ] Understand conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`)
- [ ] Manually resolve conflicts in editor
- [ ] Use merge tool (`git mergetool`)
- [ ] Configure preferred merge tool
- [ ] Stage resolved files (`git add <file>`)
- [ ] Complete merge after resolution (`git commit`)

### Conflict Prevention & Strategy
- [ ] Choose conflict resolution strategy (`git merge -X ours/theirs`)
- [ ] Abort merge when needed (`git merge --abort`)
- [ ] Reset to pre-merge state
- [ ] Preview merge without executing (`git merge --no-commit --no-ff`)

### Advanced Conflict Handling
- [ ] Resolve conflicts in binary files
- [ ] Handle conflicting file renames
- [ ] Deal with deleted file conflicts
- [ ] Resolve submodule conflicts

## 🔄 Branch Rebasing

### Basic Rebasing
- [ ] Rebase current branch (`git rebase <base>`)
- [ ] Rebase onto different branch (`git rebase --onto <new> <old> <branch>`)
- [ ] Continue rebase after conflicts (`git rebase --continue`)
- [ ] Abort rebase (`git rebase --abort`)
- [ ] Skip problematic commit (`git rebase --skip`)

### Interactive Rebasing
- [ ] Start interactive rebase (`git rebase -i <base>`)
- [ ] Squash commits during rebase
- [ ] Edit commit messages during rebase
- [ ] Reorder commits during rebase
- [ ] Drop unwanted commits
- [ ] Split commits during rebase
- [ ] Fixup commits (`git commit --fixup`)

### Rebase vs Merge Decision
- [ ] Understand when to rebase vs merge
- [ ] Use rebase for feature branches
- [ ] Use merge for integration branches
- [ ] Avoid rebasing shared branches
- [ ] Create clean, linear history with rebase

## 🏷️ Branch Tagging & Save Points

### Creating Tags on Branches
- [ ] Tag current branch tip (`git tag <name>`)
- [ ] Create annotated tags (`git tag -a <name> -m "message"`)
- [ ] Tag specific commit on branch (`git tag <name> <commit>`)
- [ ] Tag before important merges

### Using Tags as Save Points
- [ ] Create milestone tags
- [ ] Tag before risky operations
- [ ] Use tags for release candidates
- [ ] Create backup tags before branch deletion

## 🚀 Advanced Branch Operations

### Cherry Picking Between Branches
- [ ] Cherry pick single commit (`git cherry-pick <commit>`)
- [ ] Cherry pick commit range (`git cherry-pick A..B`)
- [ ] Cherry pick without committing (`git cherry-pick --no-commit`)
- [ ] Cherry pick and edit message (`git cherry-pick --edit`)
- [ ] Resolve cherry-pick conflicts

### Branch Comparison
- [ ] Compare branches (`git diff branch1..branch2`)
- [ ] Show commits in one branch but not another (`git log branch1..branch2`)
- [ ] Show commits unique to each branch (`git log --left-right branch1...branch2`)
- [ ] Find merge base (`git merge-base branch1 branch2`)

### Branch Cleanup
- [ ] Delete merged local branch (`git branch -d <branch>`)
- [ ] Force delete unmerged branch (`git branch -D <branch>`)
- [ ] Delete remote tracking branch (`git branch -dr origin/<branch>`)
- [ ] Prune deleted remote branches (`git remote prune origin`)
- [ ] Clean up all merged branches script

## 🌐 Remote Branch Operations

### Remote Branch Management
- [ ] List remote branches (`git branch -r`)
- [ ] Fetch remote branches (`git fetch origin`)
- [ ] Create local branch tracking remote (`git checkout -b <local> origin/<remote>`)
- [ ] Set upstream for existing branch (`git branch -u origin/<branch>`)
- [ ] Push new branch to remote (`git push -u origin <branch>`)

### Remote Branch Synchronization
- [ ] Push branch updates (`git push origin <branch>`)
- [ ] Pull remote branch changes (`git pull origin <branch>`)
- [ ] Force push branch (`git push --force-with-lease`)
- [ ] Delete remote branch (`git push origin --delete <branch>`)

### Tracking Remote Branches
- [ ] Set up tracking relationship
- [ ] Check tracking status (`git branch -vv`)
- [ ] Change upstream branch (`git branch --set-upstream-to`)
- [ ] Unset upstream branch (`git branch --unset-upstream`)

## 🎯 Branch Workflow Patterns

### Feature Branch Workflow
- [ ] Create feature branch from main
- [ ] Work on feature in isolation
- [ ] Keep feature branch updated with main
- [ ] Merge feature back to main
- [ ] Clean up feature branch after merge

### Git Flow Pattern
- [ ] Work with develop branch
- [ ] Create feature branches from develop
- [ ] Create release branches
- [ ] Handle hotfix branches
- [ ] Merge patterns for Git Flow

### Topic Branches
- [ ] Create focused topic branches
- [ ] Keep topic branches small and focused
- [ ] Merge or rebase topic branches
- [ ] Stack topic branches when needed

## 🛟 Branch Recovery & Troubleshooting

### Recovering Lost Branches
- [ ] Find deleted branch in reflog (`git reflog`)
- [ ] Recreate branch from reflog (`git branch <name> <reflog-entry>`)
- [ ] Recover accidentally deleted work
- [ ] Use `git fsck` to find orphaned commits

### Fixing Branch Issues
- [ ] Fix branch divergence issues
- [ ] Resolve "branch is ahead/behind" messages
- [ ] Fix corrupted branch references
- [ ] Recover from failed merges/rebases
- [ ] Reset branch to known good state

### Branch History Cleanup
- [ ] Squash multiple commits into one
- [ ] Remove sensitive data from branch history
- [ ] Split large commits into smaller ones
- [ ] Rewrite commit messages in branch
- [ ] Remove commits from branch history

---

## 🎓 Practice Scenarios

### Daily Branch Operations
- [ ] **Scenario 1**: Start work on new feature, save progress, switch to fix bug, return to feature
- [ ] **Scenario 2**: Merge feature branch, resolve conflicts, clean up
- [ ] **Scenario 3**: Rebase feature branch onto updated main, handle conflicts
- [ ] **Scenario 4**: Cherry-pick hotfix to multiple branches
- [ ] **Scenario 5**: Recover accidentally deleted branch with important work

### Team Collaboration
- [ ] **Scenario 6**: Handle simultaneous work on same feature branch
- [ ] **Scenario 7**: Integrate work from multiple team members
- [ ] **Scenario 8**: Resolve complex merge conflicts in team setting
- [ ] **Scenario 9**: Clean up messy branch history before sharing
- [ ] **Scenario 10**: Coordinate branch deletion across team

---

**Branch Operations Mastery Tracker:**
- Total items: ~85
- Completed: ___
- Percentage: ___%

**Quick Reference Commands:**
```bash
# Create and switch
git checkout -b feature/new-feature

# Save work temporarily
git stash push -m "work in progress"

# Switch and restore work
git checkout main
git checkout feature/new-feature
git stash pop

# Merge feature
git checkout main
git merge --no-ff feature/new-feature

# Clean up
git branch -d feature/new-feature
```

Remember: Master these branch operations through hands-on practice in a test repository!