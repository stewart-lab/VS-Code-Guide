# Step-by-step guide

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
- To double check the extensions have installed, navigate to the extesnions tab located in the left-hand menu ![Screenshot 2022-10-25 at 9 45 12 AM](https://user-images.githubusercontent.com/95723801/197805662-4192212e-7120-4ac5-b654-aae1b09d8de3.png)

- You will notice that there are more than four extensions installed! That is because python and the remote-dev extensions are actually bundles of extensions!

## Establishing Remote Connection

- Open the Command Palette (Cmd+Shift+P) and type "remote-ssh". You will have two options to ssh in. One being the current window and the other being a new one. I recommend the former as multiple windows can be tougher to manage. 

![Screenshot 2022-10-25 at 9 47 15 AM](https://user-images.githubusercontent.com/95723801/197806157-81e7221b-39ec-457c-b09d-a2fe4c432a18.png)

- In the next menu, select "Add new SSH Host.." and type in the ssh command to connect to the remote dev space of your choice.
- When asked what config file to update, select the one in your user path. This will be the last time you type an ssh command!
- Open the Command Palette again (Cmd+Shift+P) and type "remote-ssh", now your ssh target will be saved and you can simply hit enter and type in your password. 
- To confirm you are connected, in the bottom left of your VS Code window, you should see confirmation of your ssh target.
![Screenshot 2022-10-25 at 9 55 10 AM](https://user-images.githubusercontent.com/95723801/197808180-8fe2f023-42f2-4106-bb8f-5cb688fc0df8.png)
 

# Keyboard Shortcuts




https://code.visualstudio.com/shortcuts/keyboard-shortcuts-macos.pdf


