# Fullstack_Angular_SpringBoot_E_Commerce
A E-Commerce Single-Page Website built using Angular, Spring Boot

# Index
- [Introduction](https://github.com/widesu/Fullstack_Angular_SpringBoot_E_Commerce#Introduction)
- [How to Use](https://github.com/widesu/Fullstack_Angular_SpringBoot_E_Commerce#how-to-use)
- [How to Build](https://github.com/widesu/Fullstack_Angular_SpringBoot_E_Commerce#how-to-build)
    - [On Mac-Install Development Tools](https://github.com/widesu/Fullstack_Angular_SpringBoot_E_Commerce###on-mac---install-development-tools)

# Introduction
This is a full-stack E-Commerce Single-Page Website built using:
- Front-end: `Angular`, `TypeScript`
- Back-end: `Java`, `Spring Boot`
- Command line tool: `node`, `npm`, `nvm`
# How to use
```bash
Git clone https://github.com/WideSu/Fullstack_Angular_SpringBoot_E_Commerce.git
```
# How to build
## Install Angular
### On Mac - Install Development Tools

In this guide, we will install the following development tools

- Visual Studio Code
- nvm
- node
- npm
- tsc

#### Versions

The following software versions has been tested:

- nvm 0.35.0
- npm 7.24.0
- node 16.10.0
- tsc 4.6.4
- Angular 14
- Spring Boot 2.7.1

It is **highly recommended** that you use the versions listed above to make sure you do not encounter any issues with the course. If you choose to use other versions then the code may not work as expected.

#### Prerequisites

- git: You must have the git command-line tool installed.
    - To install git, visit: https://git-scm.com/

##### Install Visual Studio Code

Visual Studio Code is a general purpose IDE that support many programming languages. Visual Studio code has built-in support for TypeScript.

1. In a web browser, visit https://code.visualstudio.com/
2. Follow the link to download Visual Studio Code for Mac
3. Unzip the downloaded file
4. Move the Visual Studio Code app to your Applications Folder
5. In your Applications Folder, start the Visual Studio Code app

##### Install NVM

**nvm** is the [Node Version Manager](https://github.com/nvm-sh/nvm). It allows you to install multiple versions of Node on your computer. Once installed, then you can easily switch to a different version of Node. This is very useful if you want to develop/test using different versions of Node. When you are developing multiple projects, you will most likely need to support different versions of Node.

The best feature of nvm is that it makes the installation of Node very easy for Mac and Linux system. Historically, to install Node on Mac/Linux, you would have to make frequent use of the "sudo" command to elevate privileges. This was a painful and clunky process during development. Thanks the nvm, we no longer have to use "sudo" when using Node.

Also, the Node ecosystem is a fast moving target and versions change frequently. nvm makes it easy to stay up to date with the latest version of Node.

The website for nvm is: https://github.com/nvm-sh/nvm

> Note: You must have git installed before running this script.
> 

###### Install

1. Open a new terminal window
2. Enter the following commands:
    
    ```
    curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.35.0/install.sh | bash
    ```
    
    The script clones the nvm repository to `~/.nvm` and adds the source line to your profile: `~/.bashrc`.
    
    You will see output similar to the following:
    
    ```
      % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                    Dload  Upload   Total   Spent    Left  Speed
    100 13527  100 13527    0     0  62065      0 --:--:-- --:--:-- --:--:-- 62336
    => Downloading nvm from git to '/Users/luv2code/.nvm'
    => Cloning into '/Users/luv2code/.nvm'...
    remote: Enumerating objects: 286, done.
    ...
    
    => Appending nvm source string to /Users/luv2code/.bashrc
    => Appending bash_completion source string to /Users/luv2code/.bashrc
    => Close and reopen your terminal to start using nvm or run the following to use it now:
    
    ...
    
    ```
    

###### Setting Up Paths

####### Which shell am I using and how to switch shell?

**Which Shell Am I Using? How Can I Switch?**Updated March 13, 2022[mac](https://www.moncefbelyamani.com/tags/mac/) [terminal](https://www.moncefbelyamani.com/tags/terminal/) [zsh](https://www.moncefbelyamani.com/tags/zsh/) [bash](https://www.moncefbelyamani.com/tags/bash/) [homebrew](https://www.moncefbelyamani.com/tags/homebrew/) [beginner](https://www.moncefbelyamani.com/tags/beginner/)

####### **Finding your current shell**

Starting with macOS Catalina (10.15), Apple set the default [shell](https://en.wikipedia.org/wiki/Shell_(computing)) to the [Z shell](https://en.wikipedia.org/wiki/Z_shell) (zsh). In previous macOS versions, the default was [Bash](https://en.wikipedia.org/wiki/Bash_(Unix_shell)).

Each shell supports a configuration file in your macOS [Home](https://www.moncefbelyamani.com/home-is-where-the-heart-is/) folder that gets read every time you open a new terminal window (or tab). This allows the shell environment to be set up properly with your preferences, and so that the tools you depend on are ready to use.

In `zsh`, the configuration file is `~/.zshrc`. In `bash`, it’s `~/.bash_profile`. Some people might tell you to add things to your `~/.bashrc`. Thank them for their help, and teach them that `.bashrc` does not get read automatically on a Mac when you open up a new shell window.

If you’re not sure which shell you’re using, there are a couple of ways to find out. One is to run this command:

**`echo** **$0**`

It works in `bash` and `zsh`, but not in `fish`. Here’s a trick I use that should work in all shells. Type any bogus command that you know doesn’t exist, for example:

`monfresh`

The first word in the error message should be the name of the shell. In bash, you would see this:

`bash: monfresh: **command** not found`

In zsh:

`zsh: monfresh: **command** not found`

And in fish:

`fish: Unknown **command**: monfresh`

####### **Changing shells**

If you want to switch between shells to explore the differences, or because you know you want one or the other, use these commands:

- **Switch to bash**

`chsh **-s** **$(**which bash**)**`

- **Switch to zsh**

`chsh **-s** **$(**which zsh**)**`

> What the $() syntax does is it runs what’s inside the parentheses (such as which bash), saves the output, and passes it to chsh -s. This is convenient when you don’t know the exact path to the bash or zsh command.
> 

This will prompt you for your macOS password. For the change to take effect, you need to open a new terminal tab, or quit and restart your terminal app.

- **Important Note**

When you switch shells, if you expect to have the same configuration, make sure to copy the contents of `~/.bash_profile` into `~/.zshrc` or vice versa. Also look out for any code that is not compatible with both shells.

If you’re not sure how to open and edit dotfiles, or hidden files (those with filenames that start with a period, like `.zshrc`), read my [guide on opening hidden files on your Mac](https://www.moncefbelyamani.com/5-ways-to-open-hidden-files-on-your-mac/).

- Possible error scenario

If you get a message about a `non-standard shell`, that means that your shell is not listed in `/etc/shells`. This can happen after installing a shell with Homebrew, which is a reasonable thing to do because you can get a newer version than the one that came with macOS.

To make macOS aware of the Homebrew version of a shell, it needs to be added to `/etc/shells`. Here’s how you would safely add Homebrew’s `zsh`:

Find the path of the Homebrew `zsh`:

`which zsh`

Open `/etc/shells` in Sublime Text, or another code editor, but not TextEdit:

`open /etc/shells **-a** **"Sublime Text"**`

Copy and paste the output of `which zsh` at the bottom of `/etc/shells` and save the file. This will prompt you for your macOS password. Run the `chsh -s` command again, and this time it should not complain. Remember to open a new tab to see the new shell.

- **Alternative**

Another way to change shells is via the Terminal app preferences, by selecting the “Command (complete path)” radio button in the “Shells open with:” section as shown in the screenshot below:

!https://www.moncefbelyamani.com/images/Optimized-terminal_preferences.png

Note that this does not change your default login shell, which you can check by running `echo $SHELL`. You can test this by following these steps:

Set your login shell to `zsh`:

`chsh **-s** **$(**which zsh**)**`

At the top of your `~/.zshrc`, add this line:

**`echo** **"hello from zsh"**`

At the top of your `~/.bash_profile`, add this line:

**`echo** **"hello from bash"**`

If the file doesn’t exist, you can create it with `touch`:

**`touch** ~/.bash_profile`

Update your Terminal preferences to open the shell with the command `/bin/bash`, as shown in the screenshot above.

Quit and restart Terminal.

You should see “hello from bash”, but if you run `echo $SHELL`, you will see `/bin/zsh`.

I’m not sure if this affects anything while developing locally, so I would stick to the default settings and use `chsh -s` to switch shells.

If you’re not sure how to open and edit dotfiles, or hidden files (those with filenames that start with a period, like `.zshrc`), read my [guide on opening hidden files on your Mac](https://www.moncefbelyamani.com/5-ways-to-open-hidden-files-on-your-mac/).

Want more free guides like this? [Join 2700+ others](https://www.moncefbelyamani.com/newsletter/) who are saving time with every issue. Follow me on [Twitter](https://twitter.com/monfresh) for more development and automation tips.

####### Only for Z Shell (zsh) users

1. If you are using Z shell (zsh), apply the new PATH settings with:
    
    ```
    code ~/.zshrc
    ```
    
    > The code command will launch Visual Studio Code.
    > 
2. Add the following content to the `.zshrc` file
    
    ```
    export NVM_DIR="$HOME/.nvm"
    [ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
    [ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  # This loads nvm bash_completion
    
    ```
    
3. Save the file and exit the text editor.
4. Apply the changes with the following command
    
    ```
    source ~/.zshrc
    ```
    

###### Only for BASH shell users

1. If you are using BASH shell, apply the new PATH settings with:
    
    ```
    source ~/.bashrc
    ```
    
2. Update your `~/.bash_profile` file to reference your `~/.bashrc` file.
    
    ```
    code ~/.bash_profile
    
    ```
    
    > The code command will launch Visual Studio Code.
    > 
3. Your `.bash_profile` file should now be open in Visual Studio Code.
4. Add the following text to your `.bash_profile` file:
    
    ```
    if [ -r ~/.bashrc ]; then
       source ~/.bashrc
    fi
    
    ```
    
5. Save the file and exit Visual Studio Code.

###### Verify the Installation

1. Move back to your terminal window.
2. Verify the installation by typing the following command:
    
    ```
    nvm --version
    ```
    
    If the installation is successful, you will see the version number.
    
    > For details on other nvm commands, use nvm --help or see the docs: https://github.com/nvm-sh/nvm
    > 

##### Install Node

Node is the the runtime environment for executing JavaScript code from the command-line. By using Node, you can create any type of application using JavaScript including server-side / backend applications.

In this course, we'll use Node to run applications that we develop using TypeScript and Angular.

1. In your terminal window, type the following command:
    
    ```
    nvm install node
    ```
    
    You will see the following output
    
    ```
    Downloading and installing node v18.4.0...
    Downloading https://nodejs.org/dist/v18.4.0/node-v18.4.0-darwin-x64.tar.xz...
    ######################################################################## 100.0%
    Computing checksum with shasum -a 256
    Checksums matched!
    Now using node v18.4.0 (npm v8.12.1)
    Creating default alias: default -> node (-> v18.4.0)
    
    ```
    
2. Verify the node installation
    
    ```
    node --version
    ```
    
    If the installation is successful, you will see the version number
    
    > Note: The Node installation also includes npm (Node Package Manager).
    > 
3. Verify npm is installed
    
    ```
    npm --version
    ```
    
    If the installation is successful, you will see the version number.
    
    > Note: node will have a different number than npm. This is similar to a different Java JDK version number compared to Maven version number.
    > 
    > 
    > In this example, node is similar to the Java JDK. And npm is similar to Maven.
    > 

###### Switch Node Versions

> Note: This course has been tested with Node 16.10. We will install this version.
> 
1. Install and use Node 16.10
    
    ```
    nvm install 16.10.0
    nvm use 16.10.0
    ```
    

###### Install tsc

tsc is the TypeScript compiler. We use tsc to compile TypeScript code into JavaScript code. We can install the TypeScript compiler using the Node Package Manager (npm)

> Note: This course has been tested with TypeScript 4.6. We will install this version.
> 
1. In your terminal window, enter the following command
    
    ```
    npm install -g typescript@4.6.4
    
    ```
    
    The `-g` installs this as a global package. The TypeScript compiler will be available to all directories for this user.
    
2. You can verify the installation
    
    ```
    tsc --version
    ```
    
    If the installation is successful, you will see the version number.
    

That's it! You have successfully installed the development tools: Visual Studio Code, nvm, node, npm and tsc.
