---
slug: vstd-commits
title: Relational Commits
revision: 0
---

# Relational Commits
A git commit style guide deisgned to show a commit's relationship to the codebase.

## Summary
This document describes the format of commit messages using Relational Commits.

---

```
<breaking>[<scope>] <type?>: <description>
```

|     Field     | Optional | Description                                                           |
| ------------- | :------: | --------------------------------------------------------------------- |
| `breaking`    |    ✅    | A `!` to indicate a breaking change.                                  |
| `scope`       |    ❌    | The scope of the commit. This can be a file, directory, or a package. |
| `type`        |    ✅    | The type of commit. This can be `fix`, `feat` or any other type.      |
| `description` |    ❌    | A short description of the commit.                                    |

### Initialisation Commits
Initialisation commits are commits that are made to initialise a repository. They are not prefixed with a `!` and are scoped to the current branch.

```
[main] Initial Commit
```

## Examples
A commit that fixes a small bug in the `README.md` file.
```
[README] Fix a few typos
```

A commit that adds a new feature to the `src` directory.
```
[src] feat: Add unicorns 🦄🦄🦄
```

A commit that has some general cleanup in multiple directories.
```
[core/docs/src] Cleanup
```

A commit that removes a feature from the `pancakes` package.
```
![pancakes] feat: Remove syrup
```