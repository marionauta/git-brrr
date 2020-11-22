# git-brrr

Utility to remove local git branches that have already been merged.

## Usage

```sh
git brrr
```

## Configuration

The command won't delete your default branch, if set. You can check what this value is by running:

```
git config init.defaultBranch
```

You can set custom **protected branches** globally or per project. Multiple branches are separated by a `|` (pipe).

```sh
git config --global brrr.protectedBranches "develop"
git config brrr.protectedBranches "develop|staging" # Overrides global settings
```