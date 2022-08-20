# Get Your Tools Installed (Windows)

Now you'll install the required tools and software for the course. There's a lot to get through, so buckle in and get ready!

## Create Accounts

First, create accounts on the following websites, which you'll use throughout the course. Don't just create logins; recruiters often search these sites for job candidates, so be sure to provide at least a headshot and up-to-date contact information.

- [LinkedIn](https://www.linkedin.com/)

  **Note:** You should create a full profile that highlights your skills and work experience and includes a headshot.

- [GitHub](https://github.com/)

- [Stack Overflow ](http://stackoverflow.com/)

In addition, be sure to accept the invite for your section on [Slack](https://slack.com/). You will receive the link to your class-specific channel during orientation.

## Computer Specifications

The computer you will use in this course needs to meet the following requirements.

- Laptop with at least 8 GB RAM and 64-bit dual processor

  **Note:** Desktops, netbooks, thin clients, and tablets are not permitted.

- Windows 10 operating system

- 64 GB free disk space \(300 GB preferred\)

- At least 2.0 GHz CPU

- Virtualization capable \(Check BIOS settings.\)

- USB port

- Full administrator \("root"\) privileges to operating and all software

### Additional Considerations

- If you are using a work-issued computer, you may not have the permissions required to modify the system in order to complete class activities.

- Students with limited free disk space may elect to purchase a external hard drive to store software and courseware. Note that this is not a substitute for the required 64 GB of free disk space.

**Note:** If you need assistance determining these specifications, see the images below.

### Check CPU and RAM

1. Right-click on the bottom task bar and select **Task Manager** to open.

   **Note**: If you have trouble with this step, open the Start menu and type **task manager**. The icon will appear to the right.

2. Click on the **Performance** tab to view your machine's CPU statistics. Check the maximum speed and virtualization to make sure they meet the course requirements listed above.

   The image below shows an Intel I7 CPU with 2.6 GHz speed and virtualization enabled. This one happens to be a quad core, as shown on the bottom right. Generally the more cores, the faster the computer.

![1058](assets/1058.png)

Click **Memory** on the left panel of the screen to view RAM statistics. As shown in the following image, this laptop meets specifications with 16 GB and about 8 GB currently in use.

**Note:** If your computer is at 8 GB RAM and operating near full capacity at times, you may want to investigate the software that is using excessive resources.

![1059](assets/1059.png)

### Check Available Free Space

In File Explorer select **This PC**. You can also type **This PC** into the Start menu. Refer to the following image, which shows ample space available on the hard drives.

**Note:** Your laptop may have only the C: drive. This is fine, as long as it has the required available space.

![1060](assets/1060.png)

Note that most of the information above can be obtained by running the `systeminfo` command from the terminal. Launch a terminal by right-clicking the Start icon and selecting **Command Prompt**. Enter the command shown in the box below. After several seconds the results will be output.

![1061](assets/1061.png)

## Tool and Software Installations

Follow the instructions below to complete the installation process for all of the required tools.

### Google Chrome

1. If you don’t already have Chrome installed, visit the download page [here](https://www.google.com/chrome/browser/desktop/index.html).

2. Download, open, and run the installation file.

### Slack

1. Go to [Slack for Windows](https://slack.com/downloads). Click **Download**.

2. When the installation is complete, add our channel to your application.

3. Click the header of your current Slack channel.

4. Select **Sign in to another team**.

5. Enter the Slack domain provided to you during orientation.

   ![Slack3.1](assets/Install-Slack3.1.png)

6. Enter your email (the one that the Slack invite was sent to) and password.

### Git and Git Bash

1. Go to the Git [Downloads](https://git-scm.com/downloads) page. Select the download for Windows.

2. Select **On the Desktop**. This should save Git Bash to your desktop as well.

   ![GitWindows2.1](assets/Install-GitWindows2.1.png)

3. Select **Use Git from the Windows Command Prompt**.

   ![GitWindows2.2](assets/Install-GitWindows2.2.png)

4. Select **Checkout as-is, commit Unix-style line endings**.

   ![GitWindows2.3](assets/Install-GitWindows2.3.png)

5. Select **Use Windows' default console window**.

   ![GitWindows2.4](assets/Install-GitWindows2.4.png)


### SSH Keys

It's recommended that you use the following walkthrough video alongside the steps outlined below to add GitHub SSH keys:
​

[SSH Keys Video Walkthrough](https://youtu.be/Nf2Ggt3Mwgk)

To complete these steps, you will need to sign up for a [GitHub](https://github.com/) account if you haven't already.

**Step 1.** Open Bash.

**Step 2.** To make sure you don’t already have a set of keys on your computer, type the following in your Bash window. (**Note:** Copying and pasting will not work!)

   ​								`ls –al ~/.ssh`

   * If no keys pop up, move on to Step 3.

   * If keys do pop up, check that none of them are listed under `id_rsa`, like in this image:

     ![SSHKeyWindows1](assets/Install-SSHKeyWindows1.png)

   * If you find a key with a matching name, you can either overwrite it by following the next steps, or you can use the same key referenced in Step 8. If you decide not to overwrite it, you will need to remember the password tied to your key.  

**Step 3.** Enter the following command along with your email to generate your keys. 

   `ssh-keygen –t rsa –b 4096 –C "YOURGITHUBEMAIL@PLACEHOLDER.NET"`

**Step 4.** When prompted to enter a file to save the key, press **Enter**, and then enter a passphrase for your key. **Note:** You shouldn’t see any characters appear in the window while typing the password. When you’re finished, your window should look like this:

   ![SSHKeyWindows2](assets/Install-SSHKeyWindows2.png)

**Step 5.** Link your key to your machine using a tool called the ssh-agent. Run the following command in Bash to test whether the ssh-agent is running on your machine: `eval "$(ssh-agent –s)"`. Your Bash window should look like the following:

   ![SSHKey-Windows2](assets/Install-SSHKey-Windows2.png)

**Step 6.** Run the following command: `ssh-add ~/.ssh/id_rsa`

**Step 7.** When prompted, enter the passphrase associated with the key. **Note:** If you’ve forgotten this key, go back to Step 3. 

**Step 8.** To add the key to GitHub, copy the key to your clipboard by entering the following command:

   `clip < ~/.ssh/id_rsa.pub`

 - You shouldn’t see any kind of message when you run this command. If you do, make sure you entered it correctly. 

- **Note:** Do not copy anything else to your clipboard until all steps are completed. Otherwise, you’ll need to enter the copy command again.

**Step 9.** Go to GitHub's [SSH key settings](https://github.com/settings/ssh). Click **New SSH key**.

**Step 10.** When the form pops up, enter a name for your computer in the Title input. In the Key input, paste the SSH key you copied in Step 8.

**Step 11.** To add GitHub to your computer’s list of acceptable SSH hosts, type the following command in your Bash window:  `ssh –T git@github.com`.

- You should see an RSA fingerprint in your window. Enter **yes** only if it matches the one highlighted in the image below: 

![SSKey-Windows3](assets/Install-SSHKey-Windows3.png)

### VS Code

1. Go to the [setup page](https://code.visualstudio.com/docs/setup/setup-overview) on the VS Code website and select Windows as your platform.

2. When the download is complete, run the installer file (VSCodeSetup-version.exe\).

   **Note:** For a 64-bit machine, VS Code is installed under `C:\Program Files \(x86\)\Microsoft VS Code`.

## You're Done!

That's all for the installations, so give yourself a pat on the back! Installations are never fun, but just like taxes, you gotta do them.

Be sure to take a break before continuing with the rest of the prework.

## Prework Support

Looking for pre-work support? Our team of tutors are eager to help! Request a tutor session with the following steps:

1. If not already logged in to BCS, login using your credentials ***(supplied 24 hours after enrollment).***
2. Click **Support** in the top right.
3. Complete the form fields to submit your request:
   * Under **Question Category**, select "Tutor Request”
   * Under **Question Category**, select "Request a Tutor”
   * Under **Currently, Which Sessions Would You Like to Discuss?**, select “Prework assignment”. 
4. Complete the additional fields and submit your request. 