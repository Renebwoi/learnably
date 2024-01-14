# learnably
# Explain version control
    Version control is a system that tracks and manages changes to files over time, primarily used for software development.

# differentiate between git and github
    Git tracks your code locally, while GitHub stores and shares it in the cloud like a social network for developers.

# list other 3 github alternatives
    Subversion (SVN): Older centralized system still used in some organizations.
    Mercurial: Another distributed system similar to Git.
    CVS: Older centralized system, largely replaced by newer options.

# Explain the difference between git fetch and git pull
    The main difference between git fetch and git pull is in their action on your local files:

    git fetch: Downloads the latest changes from the remote repository, but keeps them separate from your current branch. It could be viewed as peeking at the newest updates without merging them into your work.
    git pull: Downloads the latest changes and also attempts to merge them into your currently checked out branch. It's like fetching and applying the updates in one step, potentially resulting in changes to your working directory.

# Explain in simple terms git rebase and the command for it
    Git rebase is a way of integrating changes from one branch to another by rewriting the history of the branch. It makes the branch look like it was created from a different commit, and applies the changes on top of it. This can help create a linear and clean history of the project.

    The basic command for git rebase is:

    git rebase <base>

    where <base> is the branch or commit that you want to rebase onto. For example, if you want to rebase your feature branch onto the latest main branch, you can do:

    git checkout feature
    git rebase main

    This will move the feature branch to the tip of the main branch, and replay the commits of the feature branch on top of it.

# Explain in simple terms git cherry-pick and the command for it
    Git cherry-pick is a way of applying the changes introduced by a specific commit from one branch to another branch. It is like copying and pasting a commit, without affecting the other commits in the branch. This can be useful for transferring bug fixes or small features between branches.

    The basic command for git cherry-pick is:

    git cherry-pick <commit>

    where <commit> is the reference of the commit that you want to cherry-pick. You can find the reference by using git log. For example, if you want to cherry-pick the commit f from the feature branch to the main branch, you can do:

    git checkout main
    git cherry-pick f

    This will create a new commit on the main branch with the same changes as the commit f on the feature branch.