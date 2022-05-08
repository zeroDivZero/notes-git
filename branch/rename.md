# RENAME

```git
-m, --move            move/rename a branch
-M                    move/rename a branch, even if target exists
```

## Example

```sh
git branch -m master main
```

This renames branch in local repo. Cannot rename remote branch; need to create new branch then delete old one.

```sh
git push -u origin main
git push origin --delete master
```

Often hosting platforms like GitHub require protected default branch per repo. If renaming this branch, go to repo settings to update before delete.
