Github instructions:
```
echo "# ENPM808x_valgrind_ex" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:muditsingal/ENPM808x_valgrind_ex.git
git push -u origin main
```

## Push an existing repo from command line
```
git remote add origin git@github.com:muditsingal/ENPM808x_valgrind_ex.git
git branch -M main
git push -u origin main
```

# Clone any Git repository and add it to your GitHub


## 1.) clone a git repo
It could be any repo.  Let's use cpp-boilerplate-v2 as an example.
```bash
git clone https://github.com/TommyChangUMD/cpp-boilerplate-v2
cd cpp-boilerplate-v2
```

## 2.) list all branches
```bash
git branch -va
```

Assume the output shows a branch called "main".

## 3.) checkout all branches you want to clone
```bash
git checkout main
git checkout <branch_name>
...
```

## 4.) list all remotes
```bash
git remote show
```

## 5.) remove the remote origin
```bash
git remote remove origin
```

## 6.) list all remote again to verify
```bash
git remote show
```

## 7.) Now, go to your GitHub and create an empty repo.  Give it any name you want.

1. Click: Profile Icon->"Your repositories"->"New" button

2. Assign a "Repository Name" (could be any name you want)

3. Click the "Create repository" button

4. Get the repo's ssh name.  For example:

```
git@github.com:TommyChangUMD/delem.git
```

## 8.) Assign the cloned repo a new remote origin
```bash
git remote add origin <the_repo_name_from_previous_step>
```

## 9.) List remote again to verify
```bash
git remote show
git remote show origin
```

## 10.) Add all branches back
```bash
git push --set-upstream origin main
git push --set-upstream origin <branch_name>
...
```

## 11.) List all branches to verify
```bash
git branch -va
```

You should now see the remote branches in the list.

## 12.) Set default HEAD branch (usually "main" )
```bash
git remote show origin
git remote set-head origin main
```

## 13.) Verify the new repo in GitHub

You should now get an identical repo in which you can modify.  How is
this different from forking a repo?  A forked repo can not be forked
in general.
