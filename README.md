1. git init lab_2
2. created a repo on GitHub then: git remote add origin git@github.com:mariakaiser/Git_lab_2.git
3.added a main.txt file with "first commit" written inside then: git add . , git commit -m"added main.txt file with first commit written inside" , git push -u origin main
4. git switch -c dev
5. added dev file, git add . , git commit -m"changed file name in dev" , git push -u origin dev
6. git switch main
7. git switch -c test
8. create test file,  git add . , git commit -m"added test branch with test file inside it" , git push -u origin test
9. git switch dev
10. git merge test
11. git switch main
12.  git merge dev -m"merge dev into main"
13. git push
Tell me how to remove them locally
14. git switch dev, git push, 
15. test is already up to date with origin test,
16. git switch main, git branch -d test ,  git branch -d dev

remotely.
15. from GitHub open the repo and click branches and click the trash icon next to the branch you want to delete

Tell me how to checkout another branch without commit changes
16.  git switch -c stash_test_branch, and add a file, git add . , git stash , switch to another branch and return to the stash_test_branch use git stash pop and your changes will return add and commit them if you want

Create an annotated tag with tagname (v1.7) .
17. git tag -a v1.7 -m"adding a tag"

Push it to the remote repository.
18.  git push origin v1.7

Tell me how to list tags.
19. git tag

Tell me how to delete tag locally
20. git tag -d v1.7

remotely
21. from GitHub open the repo and click tags and delete the tag you want



