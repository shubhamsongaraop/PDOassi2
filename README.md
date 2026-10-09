# DevOps Lab -- Experiment 2

## Perform Various Git Operations on Local and Remote Repositories Using Git Cheat Sheet

## Objectives

-   Understand the difference between Git and GitHub.
-   Differentiate between local and remote repositories.
-   Configure Git user details.
-   Perform commonly used Git operations using the Git Cheat Sheet.
-   Create, track, commit, and inspect changes in a local repository.
-   Connect a local repository to a remote GitHub repository.
-   Practice cloning, pushing, pulling, branching, and merging.
-   Understand how to identify and resolve merge conflicts.
-   Maintain project version history using Git.

## Group Details

  -----------------------------------------------------------------------
  **Field**                           **Details**
  ----------------------------------- -----------------------------------
  Assignment                          DevOps Lab -- Assignment 2

  Experiment                          Perform Various Git Operations on
                                      Local and Remote Repositories Using
                                      Git Cheat Sheet

  Student A                           Shubham Songara --- 34173

  Student B                           Sarthak Shastri --- 34169

  Student C                           Rutvij Warke --- 34184

  Repository                          `PDOassi2`

  GitHub URL                          `https://github.com/shubhamsongaraop/PDOassi2`
  -----------------------------------------------------------------------

## Git Commands Used

### 1. Configure Git

Set the name and email that Git records in commits, then verify the
configuration.

``` bash
git config --global user.name "Shubham Songara"
git config --global user.email "shubhamsongara2005@gmail.com"
git config --list
```

### 2. Initialize and Inspect a Local Repository

``` bash
git init
git status
git add README.md
git commit -m "Add assignment README"
git log --oneline
```

### 3. Connect to a Remote Repository

Replace `<repository_url>` with the URL of your GitHub repository.

``` bash
git branch -M main
git remote add origin <repository_url>
git remote -v
git push -u origin main
```

If `origin` already exists, update its URL instead of adding it again:

``` bash
git remote set-url origin <repository_url>
```

### 4. Clone, Pull, and Push

``` bash
git clone <repository_url>
git pull origin main
git add .
git commit -m "Update assignment details"
git push origin main
```

### 5. Create and Merge Branches

``` bash
git checkout -b feature1
# Make and save changes in your files
git add .
git commit -m "Add changes on feature1"

git checkout main
git merge feature1
```

### 6. View Changes and Commit History

``` bash
git diff
git log
git log --oneline
git show
git status
```

### 7. Undo or Unstage Changes

``` bash
# Discard unstaged changes in a tracked file
git restore README.md

# Remove a file from the staging area without deleting its changes
git reset README.md
```

> **Caution:** `git restore README.md` discards unstaged edits to that
> file. Use it only when those edits are no longer needed.

### 8. Resolve Merge Conflicts

When Git reports a conflict, open the affected file, locate the conflict
markers, edit the file to keep the intended content, and then stage and
commit the resolution.

``` bash
git status
# Edit the conflicted file and remove the conflict markers
git add README.md
git commit -m "Resolve merge conflict"
```

If two repositories have independent histories, Git may require:

``` bash
git pull origin main --allow-unrelated-histories
```

Use this only when the repositories genuinely have unrelated histories,
and resolve any resulting conflicts before committing.

## Observations

-   Git records changes and commit history in a local repository; GitHub
    hosts remote repositories for backup and collaboration.
-   `git status` helps identify changed, staged, and untracked files and
    indicates the current repository state.
-   Commits preserve snapshots of project changes and can be inspected
    using `git log` and `git show`.
-   Remote operations such as `git push` and `git pull` synchronize
    local and remote repository histories.
-   Branches allow work to be developed separately and merged when
    ready.
-   Merge conflicts can occur when changes overlap or repository
    histories differ; the conflicting content must be reviewed and
    resolved before the merge can be completed.

## Learning Outcomes

-   Learned the purpose of Git and the role of GitHub in remote
    collaboration.
-   Practiced configuring Git, initializing repositories, staging files,
    committing changes, and inspecting history.
-   Learned to connect local repositories to remote repositories and use
    clone, pull, and push.
-   Practiced creating branches and merging changes.
-   Learned how to inspect differences and safely unstage or discard
    changes.
-   Understood how to identify and resolve merge conflicts.

## Conclusion

This experiment provides practical experience with Git operations on
local and remote repositories using the Git Cheat Sheet. The activities
cover configuration, repository initialization, staging and committing,
remote synchronization, branching, merging, history inspection, and
conflict resolution. Update the observations and conclusion to reflect
the commands and activities actually completed by the group.

## References

-   [Git Documentation](https://git-scm.com/doc)
-   [Git Cheat Sheet](https://git-scm.com/cheat-sheet)
-   [GitHub Docs](https://docs.github.com/)
