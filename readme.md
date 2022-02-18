# Present your work with Git and Rebase

## Exercise 5 - Distribute recent changes to appropriate commits

Scenario:

- You are working on this awesome rolling Rick feature.
- Suddenly a wild pull request appears.
- Being a good teammate you decide to jump straight on to it.
- You need to check out another branch, so you need to preserve your own work somehow.
- You've heard some people like to `git stash` but that's a magic black box you think.
- Better with a solid good old commit: "WIP"!
- Time goes by... and then you come back to your own branch.
- Feeling happy with the work so far, you decide to get the changes into the appropriate logical atomic commits.
- Reviewing the WIP commit, you find it consists of four different _types of changes_:
  1. Changes to basic page layout
  2. Changes to the bouncy button style
  3. Changes to size calculations for rolling rick functionality
  4. A console log statement you don't need anymore.

Instructions for exercise:

- Checkout branch `start`.
- Create a new branch `exercise`.
- Have a look at the commits in `solution` branch.
- Soft reset the WIP commit.
- Unstage all changes.
- Reset the console log change.
- Create three separate commits for the rest of the change types.
- Rebase `exercise` branch on the "Add settings for vscode" commit
- Squash the three commits into appropriate commits.
- Solve merge conflicts!
  

Tips:

- The merge conflict may need some explanation:
  - It happens because the button isn't supposed to "exist" yet.
  - Instead there's a h1-element that should go in the "content" div instead of the button.
  - The next conflict happens with the commit that introduces the button.
  - Before the rebase process, that button-commit simply replaced one h1-element with a button.
  - But now a more complex layout-structure has appeared and it wasn't there before... so git gets confused and needs our help!
- When reordering commits it helps alot being aware of the time aspect involved.
  - What has happened before a commit, and what is going to happen later in the branch.
- [Soft reset](https://git-scm.com/docs/git-reset) the WIP commit on `exercise` branch.
- Commit only parts of the files
- Commits will be squashed, so it helps with a commit title that helps you identify the commit they will be squashed into.
- [Rebase](https://git-scm.com/docs/rebase) the `exercise` branch and squash.
- Use a GUI client such as [GitExtensions](http://gitextensions.github.io/) (Win), [Fork](https://git-fork.com/) (Mac + Win) or [GitKraken](https://www.gitkraken.com/) (Linux, Mac, Win) so that you don't have to figure out the git cli commands for doing the above.
- I've written a bit about reordering and squashing commits using GitExtensions on [my blog](https://blomholm.no/posts/how-i-git-it-basic-rebase/#change-the-order-of-the-commits)
- I've also written a bit about rebasing and solving merge conflicts using GitExtensions on [my blog](https://blomholm.no/posts/how-i-git-it-syncing/#pull-in-new-commits-from-another-branch)

[Click here for next exercise](https://github.com/kraftlauget/git-ws-6)
