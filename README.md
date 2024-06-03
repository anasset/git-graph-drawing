# Drawing Git Graphs

Your job is to create a Git history that looks like this:

```
* G
* I
*   T
|\  
| * I
* | N
|/  
* I
* T
* -
```

Use `git branch`, `git merge` and `git checkout` to create the necessary commits
to recreate the graph. You can check your work by running `./check`.

Hints:

- The letters are commit messages- you can make a commit without changing any
  files by running `git commit --allow-empty -m "T"`
- The order you make the commits in matters; work from the bottom to top. The
  first commit (`-`) has already been made, so your first commit should be `T`.
- The branch names you choose don't matter
- You can checkout a commit without resetting HEAD to eg. make a branch from it,
  but you'll need to use `git checkout main` to get back to your main thread.
- Merging makes its own commits; the top `T` is a merge commit, there's no need
  to make a separate one
- If you make a mistake, use `git reset --hard` to return to an earlier commit.
  You can run `./reset` to restart the entire exercise.
- `./check` might not show your branch until it diverges from `main`
- You can see a an example solution in `./solve` if you need more help

## Advanced

Try some more advanced graphs with `check 2` and `check 3`!

```
* G
*   I
|\  
| * T
* | B
|/  
*   R
|\  
| * A
| * N
* | C
|/  
* H
* -
```

```
*   G
|\  
| * I
* |   T
|\ \  
| * | C
| * | H
* | | E
| |/  
|/|   
* | C
* | K
|/  
*   O
|\  
| * U
* | T
|/  
* B
* -
```

These also work with `solve 2` and `solve 3`. This might take a lot of trial and
error, good luck!
