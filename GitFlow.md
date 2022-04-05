# Git Flow

## Main branches - remote
- **master**
  - Is in pair with production.
  - All development code is merged into `master` in sometime.
  - Releases start from this branch (Release Job)
  - Protected
- **develop**
  - Contains tested(?) pre-production code.
  - When the features are finished then they are merged into `develop`.
  - Have to contain everything which `master` has.
  - QA before or after merge to dev?
  - Scheduled end2end here?
  - Dev/QA env releases are possible from here.
  - Protected

## Dev branches - in forks

- **feature-***
  - Used to develop new features.
  - Has to branch off from `develop` and must merge into `develop`.
  - mandatory passing unit tests in case of PR.
  - mandatory passing end2end on PR?
  - DEV env releases are possible from here.
- **hotfix-***
  - in case of need to act immediately upon an undesired status of `master`
  - Has to branch off from `master` and must merge into `master`.
  - After merge develop need's to be rebased on `master` / Needs to be merged back to `develop` as well.
  - DEV env releases are possible from here.
- ***release-\****
  - *preparation of a new production release.*
  - *Allow many minor bug to be fixed and preparation for a release.*
  - *Has to branch off from `develop` and must `merge` into master and `develop`.*
  - *UAT releases from here*
  
 ## Action items:
 
  - Tutorial on how tos: how to push to any branch.
  - Guidance on releases.
  - Dev - master rebase guidance.
