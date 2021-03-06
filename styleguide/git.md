# Git Branching Model

Joinbox uses a more specific version of the git-flow branching model

![Alt text](https://github.com/joinbox/guidelines/raw/master/styleguide/git-flow.png "Joinbox GIT Flow")


- the master branch can be released at any time, it is always 100% stable
- the develop branch contains only code that works and is stable but not yet tested by the client
- features and bug fixes are developed in feature branches until they are stable. the base branch for creating feature branches is develop.
- feature branches may only merged into the develop branch if they are tested and work correctly
- for each iteration (release cycle, milestone) a new release branch is created from develop as soon everything is ready.
- the release branch is published to a testing server for acceptance tests by the client. the client should receive the change log of the release branch
- fixes for the release branch are merged into the release branch
- the release branch may be merged into develop or another release branch if it is required
- hot fixes are only created if they must be applied to the master branch for immediate release. they are based on the master branch
- after a hot fix was released the master branch is merged into the develop branch
- releases must be planned in advance, there should no more than one release branch at any time
- after the release branch was merged into master and tagged with the correct version the release branch may be deleted.

