# Configuring Git and GitHub on WSL2

[![GitHub Repo]( &#34;Open GitHub Repo&#34;)](https://github.com/learn-co-curriculum/phase-0-wsl2-env-git-github)[![Create New Issue]( &#34;Create New Issue&#34;)](https://github.com/learn-co-curriculum/phase-0-wsl2-env-git-github/issues/new/choose)## Create a GitHub Account

To work on and get credit for the labs and lessons that you work on during the program, you will need to sign up for a GitHub account  *if you don’t already have one* .

### Action Item

1. Open the [GitHub signup webpage** (Links to an external site.)**](https://github.com/join) at [https://github.com/join** (Links to an external site.)**](https://github.com/join)
2. Fill out the form and create your account
3. Verify the email address connected to your GitHub account

### Check Your Work

If you were able to verify your email address, continue below.

## Configure Git and GitHub

Git is the tool that we’ll use to download and upload the work we do in labs and lessons. To use Git without signing in every time, you can create a Secure Shell (SSH) key and associate that to your GitHub account. Lastly, you will want to run a few commands to make sure that when you use Git, you get the proper credit for your work. This step will ask you to do work both in your browser and your terminal.

### Action Item: Update Git

1. Open the "Ubuntu" application using the "Start" menu
2. Type `sudo add-apt-repository ppa:git-core/ppa` and press `<Enter>` to add a package repository for downloading the latest version of Git. Follow the prompts in the terminal.
3. Type `sudo apt update` and press `<Enter>` to update your local repository cache
4. Type `sudo apt install git` and press `<Enter>` to install the latest version of Git

You can check your work by typing `git --version` in the terminal. You should see a version greater than 2.30.0.

### Action Item: Configure Git

1. Open the "Ubuntu" application using the "Start" menu
2. Type `git config --global color.ui true` and press `<Enter>`
3. Type `git config --global user.name` + `<Space>` + your name and press `<Enter>` *(Note: this should be your full name, not your GitHub username, in quotes.)*
4. Type `git config --global user.email` + `<Space>` + the email address you used to sign up to GitHub and press `<Enter>`
5. Type `git config --global init.defaultBranch main` to [update the default branch name** (Links to an external site.)**](https://github.com/github/renaming) to `main`
6. Type `ssh-keygen` and press `<Enter>`, for each prompt  **do not type anything** , just continue to press `<Enter>`. It's particularly important that you **do not enter a passphase** and leave the passphrase empty when prompted; otherwise, you'll have to enter that passphrase any time you interact with GitHub (which will happen a lot during the program); and you may run into issues submitting assignments later.
7. Type `cat ~/.ssh/id_rsa.pub | clip.exe` and press `<Enter>`. This will copy your SSH key to your clipboard
8. Open the [GitHub New SSH key form** (Links to an external site.)**](https://github.com/settings/ssh/new) ([https://github.com/settings/ssh/new** (Links to an external site.)**](https://github.com/settings/ssh/new)) *(Note: you need to be logged in to GitHub to access that link.)*
9. Type "My personal PC" in the "Title" input field
10. Paste what’s on your clipboard from step seven in the "Key" input field
11. Click "Add SSH Key"

### Check Your Work

If you see your new SSH key beneath the "SSH keys" heading, continue to the next lesson,  **Verify and Troubleshoot Your WSL2 Environment Setup** .
