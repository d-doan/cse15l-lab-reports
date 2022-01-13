# Lab Report 1

In this report we will be exploring how to create log into a course specific account on ieng6 using the vscode terminal on a windows machine.

## Part 1

The first thing we have to do is to install Visual Studio Code (VSCode) a coding IDE that we will use to log into ieng6. Here is the link for the download. [VSCode download](https://code.visualstudio.com)

Once opened you should see a page similar to the image below and you should click on the dropdown caret in order to install VSCode for your specific OS.
![Image](vscode_screenshot.png)

## Part 2

Since this guide is for Windows we need to install or enable OpenSSH, provided here: [OpenSSH](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse)

After OpenSSH is enabled we now need to get our specific ieng6 account which will appear in this format `cs15lwi22zz@ieng6.ucsd.edu` with the wi22 being the current term and zz being account specific characters.

In order to do this we first need to create a password for this account which will be done through the [UCSD account lookup page](https://sdacs.ucsd.edu/~icc/index.php). We're going to login to the **Account Lookup** portion as pictured below. 
![Image](ieng6-password-reset.png)

From here we are going to scroll down and click on the button labeled cs15lwi22xxx where the x's are account specific.
![Image](ieng6-password-reset2.png)

After clicking on that button it should take you to a page where you are going to click on the **change your password** button. 

*Note the username that appears on that page will be the username required for the next step.
![Image](ieng6-password-reset3.png)

From here you are going to enter the username from the previous step and your current password. There's a box to toggle whether you want to change your MyTritonLink password also which is optional but may be theoretically useful in the case that the school decides to make everyone change their password to a 12 digit password :).
![Image](ieng6-password-reset4.png)

Now you can go take a short nap since this will take the system sometime between 15-60 minutes to update. After waking up from your nap be prepared to start (slightly) less tedious tasks.

Wakey wakey now we're going to actually start the process of ssh'ing into our ieng6 account. First thing we are going to do is open VSCode and open a new terminal, which can be done either through the Ctrl +` command or you can press the terminal tab at the top and click on New Terminal. A box should pop up on the lower half of VSCode and you're going to put in the command below but instead of zz you're going to put your course username that we found a couple steps ago

`ssh cs15lwi22zz@ieng6.ucsd.edu`

If you put in the correct account name there should be a prompt that pops up in the terminal that wants you to establish the authenticity of ieng6. In order to get past this you want to type yes into the terminal and press enter.

Next it will prompt you for your password which you should fill out with the new password you created for this account. You should be able to now access your account, but if it doesn't work maybe the system hasn't updated the password in the 15-60 minute window that we gave it earlier or you typed in the password wrong.

*Note don't worry if nothing appears as you're typing your password in, VSCode doesn't visually show you typing it in for security