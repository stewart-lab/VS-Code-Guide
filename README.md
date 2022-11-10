# Step-by-step guide

[Installation](#Installation)
[Extensions](#Extensions)
[Remote](#Remote)
[Files](#Files)
[Git](#Git)
[Keyboard](#Keyboard)


## Installation
- Navigate to VS Code's download tree → https://code.visualstudio.com/Download
- Open the browser's download list and locate the downloaded app or archive.
- If archive, extract the archive contents. Use double-click for some browsers or select the 'magnifying glass' icon with Safari.
- Drag Visual Studio Code.app to the Applications folder, making it available in the macOS Launchpad.
- Open VS Code from the Applications folder, by double clicking the icon.
- Add VS Code to your Dock by right-clicking on the icon, located in the Dock, to bring up the context menu and choosing Options, Keep in Dock.


<img width="800" alt="Screen Shot 2022-10-07 at 10 28 55 AM" src="https://user-images.githubusercontent.com/95723801/195430405-13b35008-54be-4087-bd75-45287d165f52.png">

Now would be the time to change the color scheme using the first rectangle of the startup menu. Everything else, however, we will leave for later.

## Extensions

- Open the Command Palette (Cmd+Shift+P) and type 'shell command' to find the Shell Command: Install 'code' command in PATH command.

![Screenshot 2022-10-25 at 9 25 19 AM](https://user-images.githubusercontent.com/95723801/197800498-b692e413-5634-4fdd-bd48-07e368350afc.png)

'code' will now be recognized as a shell command in both your VS Code terminal and your terminal application. This will allow us to start the application in the future from the terminal as well as streamline our extension standards. 

- Open a terminal window with the keyboard shortcut (ctrl + ~) or by navigating to the terminal drop-down menu 
- Copy and paste the code block below into the command line. This is the "Stewart Bioinformatics Group Starter Pack"  

** This list is subject to change
```
code --install-extension ms-vscode-remote.vscode-remote-extensionpack
code --install-extension ms-python.python
code --install-extension ms-python.black-formatter
code --install-extension ms-python.flake8

```
- To double check the extensions have installed, navigate to the extesnions tab located in the left-hand menu 
![Screenshot 2022-10-25 at 9 45 12 AM](https://user-images.githubusercontent.com/95723801/197805662-4192212e-7120-4ac5-b654-aae1b09d8de3.png)

- You will notice that there are more than four extensions installed! That is because python and the remote-dev extensions are actually bundles of extensions!

## Remote

- Open the Command Palette (Cmd+Shift+P) and type "remote-ssh". You will have two options to ssh in. One being the current window and the other being a new one. I recommend the former as multiple windows can be tougher to manage. 

![Screenshot 2022-10-25 at 9 47 15 AM](https://user-images.githubusercontent.com/95723801/197806157-81e7221b-39ec-457c-b09d-a2fe4c432a18.png)

- In the next menu, select "Add new SSH Host.." and type in the ssh command to connect to the remote dev space of your choice.
- When asked what config file to update, select the one in your user path. This will be the last time you type an ssh command!
- Open the Command Palette again (Cmd+Shift+P) and type "remote-ssh", now your ssh target will be saved and you can simply hit enter and type in your password. 
- To confirm you are connected, in the bottom left of your VS Code window, you should see confirmation of your ssh target.
![Screenshot 2022-10-25 at 9 55 10 AM](https://user-images.githubusercontent.com/95723801/197808180-8fe2f023-42f2-4106-bb8f-5cb688fc0df8.png)

- If you decided to ssh into the mir-49 machine, you'll see that there is a multitude of extensions installed already. It is important to understand the extensions we installed are only enabled locally. To insure all of our standard extensions are in our remote workspace, navigate back to the extension tab.
- You will see two rows: local and ssh. Navigate to the ssh row and hover over the cloud button. It says "Install local extensions in <remote workspace>" this is a valuable button to be aware of if you are traversing different remote spaces. 
![Screenshot 2022-10-25 at 10 06 18 AM](https://user-images.githubusercontent.com/95723801/197811000-cbe031f2-fa94-4cd8-914b-43c2fc5cd6c3.png)

 ## Files

- VS Code has a very robust file management system. Using the keyboard shortcut (CMD + O), the command pallette turns into your working directory where you can move both vertically and horizontally with ease. 
 
- NOTE: auto-complete is initiated with the ENTER button instead of TAB 

- As an exercise, navigate to my (jfreeman) home directory and find the VS Code subdirectory. Press 'OK' to initialize yourself into the subdirectory. You can check your success by confirming your location on the explorer tab in the left-hand menu.
 
![Screenshot 2022-11-10 at 9 53 00 AM](https://user-images.githubusercontent.com/95723801/201142519-d8a14b2c-81b0-452e-98c7-18e33314035c.png)

- Now we are going to test the extensions with a "hello world" example  

- For this tutorial we are going to use a VS CODE pyvenv that was configured in this directory. From the top level of "VS_Code" run the code below in the terminal

```  
source vs_code_standard/bin/activate

```
- This activates a python 3.9 virtual environment that stores an executable interpreter for linting and formatting

- Navigate to the vscode.py file, and in the bottom right of the VSCode window, you will see "Select interpreter" - The bottom right of the window will always contain information specific to file type. Becasue this is a ".py" file, VS Code will provide you with python specific tools (our extensions and interpreter)  

![Screenshot 2022-11-10 at 10 42 39 AM](https://user-images.githubusercontent.com/95723801/201155129-9def4098-5b38-4645-9c31-8a42d825f71c.png)

- Enter the path "/vs_code_standard/bin/python" and upon completion, the "Select interpreter" will turn into 
![Screenshot 2022-11-10 at 10 47 16 AM](https://user-images.githubusercontent.com/95723801/201156122-b3208d32-4f35-4bc5-9eff-9328ed397b81.png)

- Setting default interpreters is very helpful as different projects require different envs. VS Code has User, Remote, and Workspace specific settings to control what is interpreting your python code. Settings are located in the bottom left through the cog icon or (CMD ,) You are welcome to set the path above to your deafult interpreter, but I recommend something project specific for a permanent solution. 
 
- You should be able to write sloppy code in the vscode.py file and the linting and formatting will be taken care of! Easest example: print( "hello world") 
 
- VS Code supports side by side editing. Create a file using the explorer tab's button when hovered over the top level and add a ".py" at the end
 
![Screenshot 2022-11-10 at 10 47 16 AM](https://user-images.githubusercontent.com/95723801/201191108-0028aa58-ba1d-48a2-979c-f9a3ba5f79c6.png)

- Drag the file to the far right of the editor space for side to side comparsion. If you would rather toggle through different files, open your new file and use (CNTRL + TAB) to cycle through. 
 

## Git

- Lets connect our GitHub account to VS Code. Navigate to the bottom left of the screen to the user icon. Click the "sign-in to Sync settings" button. 
 
- You will be prompted to sign in to Microsoft or GitHub in the command pallete
![Screenshot 2022-11-10 at 1 49 29 PM](https://user-images.githubusercontent.com/95723801/201192201-cbfb7405-a25e-4b1b-8b49-5d83796e879c.png)

- After following the prompts, you should navigate to the source control tab in the left hand menu ![Screenshot 2022-11-10 at 1 50 18 PM](https://user-images.githubusercontent.com/95723801/201192359-8c8dfef0-fae7-499f-90c2-a3ba8e4e377b.png)

- Now we can intialize repos similar to the "git init" command. 
 
- To avoid git from tracking large, unwanted files, initiliaztion should occur in project specific subdirectories
 
- Now, in the command pallette (CMD + SHIFT + P), we can type "git" and the different source control options are accesible from the command pallette.
 
- Read more: https://code.visualstudio.com/docs/sourcecontrol/overview
 
 
 

 
 
# Keyboard




https://code.visualstudio.com/shortcuts/keyboard-shortcuts-macos.pdf


