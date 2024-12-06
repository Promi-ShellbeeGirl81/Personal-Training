### Step 1: Open the terminal and go to the folder location of the repo you want to push

```bash
cd /Downloads/Personal-Training
```

### Step 2: Check the status of untracked or modified files
```bash
git status
```
### Step 3: If you want to add all the modified files
```bash
git add .
```
### Or if you want to add a specific file

```bash
git add <file-name>
```

### Step 4: Commit your changes with a message

```bash
git commit -m "Your commit message describing the changes"
```

### Step 5: Push the changes to the remote repository

```bash
git push origin main
```
If you're working on a different branch, replace main with the name of your branch.
