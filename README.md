# CSC_Demo Git and GitHub Setup Guide

This guide will help you install Git, configure it, and clone repositories from GitHub.

## 1. Installing Git

### On Windows:
- Download Git from the official website: [https://git-scm.com/downloads](https://git-scm.com/downloads)
- Run the installer and follow the setup instructions.
- Use **Git Bash** to execute Git commands.

### On macOS:
- Open the terminal and run:
  ```bash
  brew install git
  ```
  If Homebrew is not installed, first install it by following the instructions at [brew.sh](https://brew.sh/).

### On Linux:
- Use your package manager. For example, on Ubuntu:
  ```bash
  sudo apt update
  sudo apt install git
  ```

## 2. Configuring Git

After installing Git, set your username and email:

```bash
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"
```

This is necessary so your commits are properly identified.

## 3. Creating a GitHub Account

- If you don't already have a GitHub account, sign up at [https://github.com/join](https://github.com/join).

## 4. Generating an SSH Key (Optional)

For secure authentication without typing your password every time, generate an SSH key.

1. Generate the SSH key:
   ```bash
   ssh-keygen -t ed25519 -C "your-email@example.com"
   ```

2. Start the SSH agent:
   ```bash
   eval "$(ssh-agent -s)"
   ```

3. Add your SSH private key to the SSH agent:
   ```bash
   ssh-add ~/.ssh/id_ed25519
   ```

4. Copy your public key to the clipboard:
   ```bash
   cat ~/.ssh/id_ed25519.pub
   ```

5. Go to **GitHub > Settings > SSH and GPG keys > New SSH key** and paste the key.

## 5. Cloning a GitHub Repository

To clone a repository from GitHub, use the `git clone` command followed by the repository URL.

### Example using SSH:
```bash
git clone git@github.com:username/repository-name.git
```

### Example using HTTPS:
```bash
git clone https://github.com/username/repository-name.git
```

## 6. Basic Git Commands

Here are some commonly used Git commands to get you started:

- **Check the status of the repository:**
  ```bash
  git status
  ```

- **Add files to the staging area (before committing):**
  ```bash
  git add <file-name>
  ```
  To add all files:
  ```bash
  git add .
  ```

- **Commit your changes:**
  ```bash
  git commit -m "Your commit message"
  ```

- **Push your changes to GitHub:**
  ```bash
  git push origin main
  ```
  Replace `main` with `master` if you're using the `master` branch.

---

Now you're ready to start working with Git and GitHub!

