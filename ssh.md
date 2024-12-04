# Setting Up SSH for GitHub

## Step 1: Verify Your SSH Key Exists
Check if an SSH key has already been created:

```bash
ls ~/.ssh
```

If you see files like id_ed25519 or id_rsa, proceed to Step 2.
If no key exists, generate one:

```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```

Replace "your_email@example.com" with your GitHub email.
Follow the prompts to save the key (press Enter to accept the default location).

## Step 2: Add the SSH Key to the SSH Agent
Start the SSH agent:

```bash
eval "$(ssh-agent -s)"
```

```bash
ssh-add ~/.ssh/id_ed25519
```

## Step 3: Add Your SSH Key to GitHub
Copy the Public Key:

```bash
cat ~/.ssh/id_ed25519.pub
```

If using RSA:
```bash
cat ~/.ssh/id_rsa.pub
```
Copy the output of the command.

Add the Key to GitHub:
Go to GitHub > Settings > SSH and GPG keys > New SSH key.
Add a title (e.g., "My Device") and paste the key into the field.
Click Add SSH key.

## Step 4: Test the SSH Connection
Run the following:
```bash
ssh -T git@github.com
```
If successful, you’ll see:
```bash
git clone git@github.com:Promi-ShellbeeGirl81/Personal-Training.git
```

