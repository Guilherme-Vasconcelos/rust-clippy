# Personal git hooks

Just some hooks I use during clippy development. Feel free to use them if you wish!

## Installation

If you're modifying the hooks, I recommend you install them by using a symlink, this way you won't need to
copy it to correct path every single time. From `.git/hooks`, run the command:

```sh
$ ln -s -f ../../personal/check_toml_changes ./post-merge
$ ln -s -f ../../personal/check_toml_changes ./post-rewrite
```

If you're not modifying the hooks (i.e. you're on a branch that doesn't have the `personal` folder) you can
just copy or move the hooks into `.git/hooks/` so it won't be tracked by git when you perform a commit:

```sh
$ cp ./personal/check_toml_changes ./.git/hooks/post-merge
$ cp ./personal/check_toml_changes ./.git/hooks/post-rewrite
$ git checkout something-else  # now `personal` doesn't exist, but the hook has already been copied
```
