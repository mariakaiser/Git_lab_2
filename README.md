<img width="300" height="300" alt="61rFp63+xsL _AC_SY300_SX300_QL70_FMwebp_" src="https://github.com/user-attachments/assets/e64d6ae8-5e49-4a8e-b60a-70210a87f93a" />
# Git Lab 2

Notes and commands from Git Lab 2, covering repositories, branches, merging, stashing, and tags.

Remote repository: `git@github.com:mariakaiser/Git_lab_2.git`

---

## 1. Setup and First Commit

1. Initialize the repository:
   ```bash
   git init lab_2
   ```
2. Create a repo on GitHub, then add it as the remote:
   ```bash
   git remote add origin git@github.com:mariakaiser/Git_lab_2.git
   ```
3. Add a `main.txt` file with "first commit" written inside, then:
   ```bash
   git add .
   git commit -m"added main.txt file with first commit written inside"
   git push -u origin main
   ```

## 2. Branches

4. Create and switch to the `dev` branch:
   ```bash
   git switch -c dev
   ```
5. Add a dev file, then:
   ```bash
   git add .
   git commit -m"changed file name in dev"
   git push -u origin dev
   ```
6. Go back to `main`:
   ```bash
   git switch main
   ```
7. Create and switch to the `test` branch:
   ```bash
   git switch -c test
   ```
8. Create a test file, then:
   ```bash
   git add .
   git commit -m"added test branch with test file inside it"
   git push -u origin test
   ```

## 3. Merging

9. Switch to `dev`:
   ```bash
   git switch dev
   ```
10. Merge `test` into `dev`:
    ```bash
    git merge test
    ```
11. Switch to `main`:
    ```bash
    git switch main
    ```
12. Merge `dev` into `main`:
    ```bash
    git merge dev -m"merge dev into main"
    ```
13. Push:
    ```bash
    git push
    ```

## 4. Removing Branches

### Locally

14. Switch to `dev` and push:
    ```bash
    git switch dev
    git push
    ```
15. `test` is already up to date with `origin/test`.
16. Switch to `main` and delete the branches:
    ```bash
    git switch main
    git branch -d test
    git branch -d dev
    ```

### Remotely

15. From GitHub, open the repo, click **Branches**, and click the trash icon next to the branch you want to delete.

## 5. Checking Out Another Branch Without Committing Changes (Stash)

16. Create a branch, add a file, and stash it:
    ```bash
    git switch -c stash_test_branch
    # add a file
    git add .
    git stash
    ```
    Switch to another branch and return to `stash_test_branch`, then use:
    ```bash
    git stash pop
    ```
    Your changes will return. Add and commit them if you want.

## 6. Tags

### Create an annotated tag (`v1.7`)

17.
```bash
git tag -a v1.7 -m"adding a tag"
```

### Push it to the remote repository

18.
```bash
git push origin v1.7
```

### List tags

19.
```bash
git tag
```

### Delete a tag locally

20.
```bash
git tag -d v1.7
```

### Delete a tag remotely

21. From GitHub, open the repo, click **Tags**, and delete the tag you want.

---

## Command Quick Reference

| Command | Purpose |
|---|---|
| `git init` | Initialize a repository |
| `git remote add origin <url>` | Link a remote repository |
| `git add .` | Stage all changes |
| `git commit -m"msg"` | Commit staged changes |
| `git push -u origin <branch>` | Push a branch and set upstream |
| `git switch -c <branch>` | Create and switch to a new branch |
| `git switch <branch>` | Switch to an existing branch |
| `git merge <branch>` | Merge a branch into the current one |
| `git branch -d <branch>` | Delete a local branch |
| `git stash` / `git stash pop` | Shelve and restore uncommitted changes |
| `git tag -a <tag> -m"msg"` | Create an annotated tag |
| `git push origin <tag>` | Push a tag to the remote |
| `git tag` | List tags |
| `git tag -d <tag>` | Delete a local tag |


