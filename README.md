# hydra-flow
Github workflow built for teams with high-frequency release cycle. The command-line tool is coming soon!

## Overview
- All working features is in the `master` branch
- Modifying source code has to be done by creating new branch using the pattern `<type>/<name>`
- Creating new features/fixes will always push to `origin` remote for team members to keep track of features in progress
- After finishing the feature,
  - pull from `origin master` (conflict will be resolved here)
  - push the changes to `origin`
  - switch to `master` branch and merge the feature branch
  - delete both local and remote feature branches

## Usage
- `hydra do <type> <name>` to create new feature branch e.g. `hydra do feature localization` or `hydra do fix issue14532`
- `hydra done` to finish the current feature branch
- `hydra try staging` merges the current feature to `staging` branch and push to `origin`
- `hydra clear staging` delete the `staging` branch and checkout `master` branch as new `staging` branch

## Reference
- use [batsh](https://github.com/BYVoid/Batsh) for development
