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
* Use 'active'/ 'action' verbs in your message, that are short yet descriptive
  * Here is a BAD commit message
  > changes made to readme
  * Here is an example of a better commit message
  > Added personal ident info: name, gitname, semester

See resources for into on Git Commit

**NOTICE**: All assignments will need to have _at least_ three commits to earn full points. Most assignments will have many more than that (this is the only one who reaching three may be limited).

## Part 1 - SSH 
👉🏽 **Task**  SSH into the Khoury servers, and (optionally) setup your public/private keys for future use.  You will take a screenshot and submit that screenshot as proof of completion. 

1. You will want to use SSH from your local computer to log into Khoury servers. 
   1. For mac and linux it is already built in
   2. For windows it depends on your version, however for 10 and 11 it is built into windows via OpenSSH
2. (optional) After logging in once, you will want to use the resources below to setup your **ssh keys**. 
   1. While optional it is highly recommended to make your workflow easier
3. Once Logged into the khoury linux servers, type `pwd` and hit return.
   * `pwd` is a linux command that shows you the absolute path of your current (present) working directory
   ![SSH Login Example]
4. Create a directory for storing your assignments for example, `cs5008`
5. Take a screenshot, and save it as `ssh_login_lastname.png` where *lastname* is your last name.
   * ❗Important: This screenshot will be stored in your git repository (see below), but for now, store it locally on your computer to copy later.

## Part 2 - Github



## 📝 Grading Rubric


Add (AG) and (MG) next to tiers, add major conditions to meet to pass each tier. 

1. Learning ()
   * 
2. Approaching  ()
   * 
3. Meets  ()
   * 
4. Exceeds  ()
   * 


AG - Auto-graded  
MG - Manually graded

## Instruction Home
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
There is also a program you can install with app-get or brew. ssh-copy-id

```console
> ssh-copy-id USERNAME@login.khoury.northeastern.edu
```
### Visual Studio Code Remote

* [VSCode Remote Development Pack](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack)
* [VSCode Remove Repositories](https://marketplace.visualstudio.com/items?itemName=ms-vscode.remote-repositories)
* [Using VSCode Remote Tutorial](https://dev.to/phiilu/use-visual-studio-code-remote-to-edit-files-on-servers-382i) - note you may want to follow the key setups above as compared to the ones presented in the tutorial.


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

<!-- Link definitions-->
[SSH Login Example]: ssh_login_example.png
