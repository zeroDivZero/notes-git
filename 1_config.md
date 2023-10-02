# `config`

`git config` sets configurations of how Git looks and operates. Found in 3 places:

* `/etc/gitconfig`: For every user and repo. Pass `--system` to access this file.
* `~/.gitconfig` or `~/.config/git/config`: Specific to user. Pass `--global` to access.
* Config file in Git directory (`.git/config`): Specific to that repo.

Each level overrides previous, so values in `.git/config` trump those in `/etc/gitconfig`.

## User Identity

Should set username and email. Immutably baked into every commit:

```sh
git config --global user.name "Ellis Smith"
git config --global user.email ellissmith@example.com
```

## Check Settings

To list all settings:

```sh
git config --list
```

Keys may appear multiple times if they appear in different files. Last value used.

To check specific value:

```sh
git config user.name
```

## Editor

Git uses system's default text editor. To change:

```sh
git config --global core.editor vim
```

## Default Branch

Default branch may be `master` if not set (when running `git init`):

```sh
git config --global init.defaultbranch main
```
