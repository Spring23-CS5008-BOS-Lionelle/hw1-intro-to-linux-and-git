# Homework 01 - Introduction to Linux and Git - Instructions

For this assignment, you will be exploring Linux, the Khoury servers, and GIT. For this assignment, you will
need to make sure the following is in place

1. You have a Khoury Account Setup 
   * [Apply](https://my.khoury.northeastern.edu/account/apply) and 
   * Test your [profile](https://my.khoury.northeastern.edu/session/login)
2. Have your Github.com Account Setup ([Instructions](https://docs.github.com/en/get-started/signing-up-for-github/signing-up-for-a-new-github-account))
   * Free account is fine
   * We recommend a professional email that is not tied to a school, so your account exists after you graduate.
3. If you haven't already, in your canvas shell you will be provided with a Github classroom link that will
let you use this repository as a template for your work. 

## GIT Commit
Throughout this assignment you will be committing your changes to your repository. When you commit to Git.
* Commit frequently after every major change
* Use active/action verbs in your message, that are short yet descriptive
  * Here is a BAD commit message
  > changes made to readme
  * Here is an example of a better commit message
  > Added personal ident info: name, gitname, semester

See resources for into on Git Commit

**NOTICE**: All assignments will need to have _at least_ three commits to earn full points. Most assignments will have many more than that (this is the only one who reaching three may be limited).


> Lastly, but most importantly, this assignment will require you to search online for solutions. That is part of the learning process with computer science, so give yourself time to do it all!

## Part 1 - SSH 
👉🏽 **Task**:  SSH into the Khoury servers, and (optionally) setup your public/private keys for future use.  You will take a screenshot and submit that screenshot as proof of completion. 

1. You will want to use SSH from your local computer to log into Khoury servers. 
   1. For mac and linux it is already built in
   2. For windows it depends on your version, however for 10 and 11 it is built into windows via OpenSSH
2. (optional) After logging in once, you will want to use the resources below to setup your **ssh keys**. 
   1. While optional it is highly recommended to make your workflow easier
3. Once Logged into the khoury linux servers, type `pwd` and hit return.
   * `pwd` is a linux command that shows you the absolute path of your current (present) working directory
   ![SSH Login Example]
4. Create a directory for storing your assignments. For example: `cs5008`
5. Take a screenshot, and save it as `ssh_login_lastname.png` where *lastname* is your last name.
   * Important❗ This screenshot will be stored in your git repository (see below), but for now, store it locally on your computer to copy later.

## Part 2 - Github
> This part assumes you have already clicked on the Github Classroom link in canvas. Doing so it will
> create a repository specific to your account. 

👉🏽 **Task**: You will clone your assignment repo, update your readme file, and make your first commit. 

### Cloning the Repo
1. On the Khoury servers, change directory (`cd`) into the directory you created. 
2. Find the clone url for your *personal* repository in the github classroom by clicking on the code button, and then copy.
   ![Clone Example]
   * IMPORTANT❗  Double check that it is your personal repo, and not the general assignment repo. 
3. On the command line, type the following:
   ```console
   > git clone "<the link you just copied>"
   for example
   > git clone https://github.com/Spring23-CS5008-BOS-Lionelle/lionelle-spring23-hw1.git
   ```

### Updating the README.md
1. You should now update the README.md name, and github account name 
2. Commit your repo 
3. Push update to github
   *  ➡️ If done properly, you will be able to see the changes by going to the link in a browser

#### Editing README.md
Have two options
1. Use one of the command line editors such as Vim, Emacs, or Nano.  Vim is used in many of the videos but so are the others. Even different faculty have different preferences. I personally used emacs for years. 
2. Use VSCode remote features to write and save to the file

It is worth trying both options. The first is great for quick edits, but you may find the later easier for larger projects. See additional resources to help you out with both options.

#### Pushing update to Github
For pushing your update to github you have a couple options based on the method.

1. Using VSCode, you should be able to click on Source Control Tab (Cntl+Shift+G and G), and click commit and sync/push. It will run you though authorizing github with VS code.
2. Using the command line, since you don't have access to a GUI, you will need to setup a Personal Access Token. Follow this [guide](pat_guide.md) by Professor Logan Schmidt.



## Part 3 - Linux Practice

For this part, you will be practicing with a few linux commands. After each set, you will be adding screenshots to your repo, and committing the changes for each step!


### 👉🏽 **Task**: Create a .bash_profile
In your **home** directory on the linux server (`cd ~` to get there).

1. Use a command line program  to create a .bash_profile file  
   ```console
   > nano .bash_profile
   ```
2. Update the PS1 variable in the file. You have a number of options, here is one suggested option
   ```text
   export PS1="\u:\w> "
   ```
   The above tells you which login you are using, and your current working directory (~ is a shortcut for your $HOME directory).
3. You can add other features by looking around. Be careful as a lot of searches bring up macOS specific bash_profile suggestions. Alias's are the common suggestions. When done, make sure to run
   ```console
   > source .bash_profile
   ```
   This will reload your new settings. 
4. Copy (`cp`) the .bash_profile you created to your repo directory. You will turn it in. The only thing required is updating the prompt (PS1).

Make sure to commit your changes to your repo!

### 👉🏽 **Task**: Practice with curl and grep
You will be pulling files from online, searching them, and getting stats about them. You will need to take various screenshots of the process

In your repo directory:
1. Using the `curl` command, get the following [file](https://shakespeare.folger.edu/downloads/txt/a-midsummer-nights-dream_TXT_FolgerShakespeare.txt) and save it as `midsummer-dream.txt`
2. Run the `tail` command on the copied file.
3. Take a screenshot showing both tasks have been completed, and add the screenshot to your repo directory (good place to commit)
   * Depending on how you are accessing your directory, you may have to play with ways on getting the screenshot to the repo!
   * To confirm you did it correctly, here is what the output with your own command prompt should look like:
   ```text
   lionelle:~/cs5008/hw1-lionelle>tail midsummer-dream.txt
        If you pardon, we will mend.
        And, as I am an honest Puck,
        If we have unearned luck
        Now to 'scape the serpent's tongue,
        We will make amends ere long.
        Else the Puck a liar call.
        So good night unto you all.
        Give me your hands, if we be friends,
        And Robin shall restore amends.
   [He exits.]
   ```
4. `grep` the file for the word dream, storing the output of the grep command to the file `dream.txt`
5. Run `wc` on dream.txt (it should display "16 131 753 dream.txt" if you did it correctly)
6. Run `cat` on `dream.txt`
7. Take a screenshot of your command prompt showing these three commands, adding it to the repo (along with dream.txt)
8. This would be a good place to commit and push your repo!


## Don't forget
👉🏽 **Task**: If you haven't yet, add your screenshot from **part 1** to the repo, and commit and push the changes. 

As a reminder, your files need to be in the base of the repo (not the instructions directory - this is provided so you have a local copy of the instructions).


## 📝 Grading Rubric

While many of your assignments will have an autograded and manually graded component, due to the nature of this assignment everything is manually graded. As a reminder, review the syllabus to see how Tier Mastery grading works.  You may submit more than once. 

### To Submit
Click on the Gradescope link on the sidebar of the Canvas course. Select CS 5008, and select Homework 01. Ideally, you follow the link at the bottom of the assignment page. 

On Gradescope, select that you want to submit your code via Github, and connect your Github account with Gradescope. You'll need to authorize Gradescope to have access to your account. 

⭐ Make sure your repo has the files you need to turn in! Grade Scope will pull from Github. 

1. Learning (MG)
   * Student has setup their github account, and is able to submit files from their repo (even if it is an empty unchanged repo)
2. Approaching  (MG)
   * Screenshot documenting ability to log into the Khoury servers via SSH
3. Meets  (MG)
   * .bash_profile created along with screenshot showing it's use. 
4. Exceeds  (MG)
   * curl/grep command sequence completed with associated files and screenshots
   * repo README.md fully updated


AG - Auto-graded  
MG - Manually graded

### Instruction Home
Please note, if you are viewing these instructions in your repository copy, it is possible for your local copy to be out of sync with the official instructions. 
Double check instructions by going to: [HW 1 - Instructions](https://github.com/Spring23-CS5008-BOS-Lionelle/hw1-intro-to-linux-and-git)

## 📚 Resources

### Git
* [Git Handbook](https://docs.github.com/en/get-started/using-git/about-git) -- start here
* [clone](https://github.com/git-guides/git-clone)
* [commit](https://github.com/git-guides/git-commit)
* [add](https://github.com/git-guides/git-add)
* [push](https://github.com/git-guides/git-push)
* [How to Write Better Commit Messages](https://www.freecodecamp.org/news/how-to-write-better-git-commit-messages/)

### SSH Key
* [What are SSH Keys](https://www.w3docs.com/learn-git/ssh-key.html)
  * Note: the line about windows is incorrect since windows 10. You can run ssh-keygen directly via powershell (see below)
* [How To Generate SSH Keys on Windows 10+](https://www.howtogeek.com/762863/how-to-generate-ssh-keys-in-windows-10-and-windows-11/)

### Adding SSH Public Key to Remote Server

* [Linux/Mac: How to add public SSH key on a remote server](https://www.howtogeek.com/168147/add-public-ssh-key-to-remote-server-in-a-single-command/)

#### Windows Upload Command
There are multiple ways to upload your public key to your remote server. The easiest simply being logging into the server and cutting and pasting the key into authorized_keys. However, the following command line will do that for you (make sure to make changes)

```console
> ssh USERNAME@login.khoury.northeastern.edu "umask 077; test -d .ssh || mkdir .ssh ; cat >> .ssh/authorized_keys2 || exit 1" < PATH-ON-WINDOWS\id_rsa.pub
```

The PATH-ON-WINDOWS is the path to your public key. Often it will be C:\Users\YOUR_WINDOWS_USER_NAME\.ssh\id_rsa.pub as that is the default location when you run keygen. 

#### Linux and Mac Upload Command
There is also a program you can install with app-get or brew. `ssh-copy-id`

```console
> ssh-copy-id USERNAME@login.khoury.northeastern.edu
```
### Visual Studio Code Remote

* [VSCode Remote Development Pack](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack)
* [VSCode Remove Repositories](https://marketplace.visualstudio.com/items?itemName=ms-vscode.remote-repositories)
* [Using VSCode Remote Tutorial](https://dev.to/phiilu/use-visual-studio-code-remote-to-edit-files-on-servers-382i) - note you may want to follow the ssh-key setup above as compared to the ones presented in the tutorial.


### Command Line Editors
* Vim - use `vimtutor` via the command line on the Khoury servers
* [Vim School](https://vimschool.netlify.app/)
* [Very basic emacs](http://ocean.stanford.edu/research/quick_emacs.html)
* [Emacs](https://www.gnu.org/software/emacs/tour/)
* Emacs has a built in tutorial
   * type emacs on the command line emacs   
   * then type control-h followed by t
* [Redhat Beginning Guide to Emacs](https://www.redhat.com/sysadmin/beginners-guide-emacs)
* [Guide to Nano](https://www.howtogeek.com/howto/42980/the-beginners-guide-to-nano-the-linux-command-line-text-editor/)


### Linux
* [Customize Bash Prompt in Linux](https://phoenixnap.com/kb/change-bash-prompt-linux)
* [50 Linux Commands with examples](https://www.puttygen.com/linux-commands)

<!-- Link definitions-->
[SSH Login Example]: ssh_login_example.png
[Clone Example]: clone_example.png
