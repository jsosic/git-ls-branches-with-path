# git-ls-branches-with-path

Git script to list all the branches that contain modifications to any file in
the specified path

## Description

Prints the list of all the branches that contain modified files within the
designated path.

## Installation

Copy the `git-ls-branches-with-path` file anywhere inside your path,
and chmod it to `0755`.

## Examples

When there are branches that contain modified file, you will get the following
output:

```
% git ls-branches-with-path aws/staging/lb.tf
Searching for path: "aws/staging/lb.tf" in remote branches.
Path "aws/staging/lb.tf" was modified in the following branches:
 - TEAM-723-add-new-uri
 - refactor-lb
```

If file is not modified in any of the branches, output should look like this:

```
% git ls-branches-with-path aws/staging/my-other-lb.tf
Searching for path: "aws/staging/my-other-lb.tf" in remote branches.
Path "aws/staging/my-other-lb.tf" was not modified in any of the remote branches.
```

Path can also be a directory.
