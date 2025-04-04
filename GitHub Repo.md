# GitHub Repo

## Step 1 — Create a new GitHub Repo

create GitHub repository 

## Step 2 — Initialize Git in the project folder

From your terminal, run the following commands after navigating to the folder you would like to add.

### Step 3 - Initialize the Git Repo

```powershell
git init
```

### Add the files to the Git index

```powershell
git add -A
```

### Commit Added Files

```powershell
git commit -m 'Added my project'
```

### Add a new remote origin

```powershell
git remote add origin git@github.com:sammy/my-new-project.git
```

### Push to GitHub

```powershell
git push -u -f origin main
```

## All together

```powershell
git init
git add -A
git commit -m 'Added my project'
git remote add origin git@github.com:sammy/my-new-project.git
git push -u -f origin main
```
