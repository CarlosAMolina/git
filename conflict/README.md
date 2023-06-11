## Introduction

Folder to work with Git conflicts.

## How it works

### Create a conflict

To create a conflict:

```bash
git checkout main
git merge feature/conflict
```

Now you have a conflict to manage.

### Resolve conflicts with Fugitive Vim plugin

After create the conflict in the `src/test.md` file we can manage it.

Open the file:

```bash
vi src/test.md
```

Open the conflict resolution screen:

```bash
:Gvdiffsplit!
```

Resolve conflicts. Example:

- Go to next conflict:

  ```bash
  ]c
  ```

- Accept left screen option:

  ```bash
  :diffget //2
  ```

- Accept right screen option:

  ```bash
  :diffget //3
  ```

When there are no more conflicts save the changes:

```bash
:xa
```

Resource: <https://medium.com/prodopsio/solving-git-merge-conflicts-with-vim-c8a8617e3633>
