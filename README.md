# git-brrr

Utility to remove local git branches that have already been merged.

## Usage

```sh
git brrr
```

## Install

Clone this repo and make sure the `git-brrr` file has executable permissions.

```sh
git clone https://github.com/marionauta/git-brrr
cd git-brrr
chmod +x git-brrr
```

Then, move the `git-brrr` file to somewhere in your PATH. That means, move it to some directory listed afer running:

```sh
echo $PATH | tr ":" "\n"
```

## Configuration

The command won't delete your default branch, if set. You can check what this value is by running:

```sh
git config init.defaultBranch
```

You can set custom **protected branches** globally or per project. Multiple branches are separated by a `|` (pipe).

```sh
git config --global brrr.protectedBranches "develop"
git config brrr.protectedBranches "develop|staging" # Overrides global settings
```