**Dev Containers tutorial** <br>
This guide provides step-by-step instructions for running Visual Studio Code within a Docker container by utilizing the Dev Containers extension. You don't require any prior Docker knowledge to follow along with this tutorial.
Utilizing a Docker container to run VS Code offers various advantages, but in this tutorial, our primary emphasis is on using a Docker container to establish a distinct development environment that is isolated from your local setup.

**Prerequisites** <br>
   Visual Studio Code

**Install Docker** <br>
   To produce and oversee your containers, you require Docker.

- **Docker Desktop** <br>
   Obtain and install Docker Desktop, or explore other Docker alternatives such as Docker on a remote host or Docker-compatible CLI.
  
- **Start Docker** <br>
   Launch the Docker Desktop application to initiate Docker. You can confirm its operation by checking the activity tray, where you'll 
   spot the Docker whale icon. <br>
   It's worth noting that Docker might require a couple of minutes to start.
   If you observe an animated whale icon, it's likely still in the startup phase. You can click on the icon to access the status 
   information.
  
   ![image](https://github.com/Sruti-sahini/Python/assets/100782959/62137a1d-b712-45e1-a85e-e5f06c47052c)

- **Check Docker** <br>
    Once Docker is running, you can confirm that everything is working by opening a new terminal window and typing the command:
  
    ```
    docker --version
    # Docker version 18.09.2, build 6247962
    ```

- **Install the extension** <br>
    With the Dev Containers extension, you can execute Visual Studio Code within a Docker container.

    ![image](https://github.com/Sruti-sahini/Python/assets/100782959/cd8c7605-06c1-4af8-a3ff-f257d11674e0)

- **Check installation** <br>
    With the Dev Containers extension installed, you will see a new Status bar item at the far left.

    ![image](https://github.com/Sruti-sahini/Python/assets/100782959/8544e47d-db46-4b6d-a7e6-401a573227a8)

    The Remote Status bar item provides a rapid way to indicate whether VS Code is operating in a local or remote context. Clicking on 
    this item will display the Dev Containers commands.

    ![image](https://github.com/Sruti-sahini/Python/assets/100782959/61a0fd91-e377-4bca-8bb0-2d9c8d53414f)

- **Get the sample** <br>
    To create a Docker container, start by opening a GitHub repository containing a Node.js project. <br>
    Access the Command Palette by pressing F1, then execute the "Dev Containers: Try a Dev Container Sample..." command and select the 
    Node sample from the list. <br>
    **Note** - Please be aware that there are alternative development container samples available, such as vscode-remote-try-python or 
    vscode-   remote-try-java. However, this guide specifically focuses on using vscode-remote-try-node.

- **Wait for the container to build** <br>
    Subsequently, the window will refresh. However, because the container hasn't been established yet, VS Code will proceed to create it 
    and duplicate the sample repository into a separate container storage space. This operation might consume some time, and a progress 
    notification will furnish you with ongoing updates. Fortunately, on future folder openings, this step won't be required, as the 
    container will already be in place.

    ![image](https://github.com/Sruti-sahini/Python/assets/100782959/a1926f54-5c02-4397-9888-09a24b864435)

    Once the container is constructed, VS Code will seamlessly link to it and establish a connection, facilitating the mapping of your 
    project folder from the local file system into the container.

- **Check the container** <br>
    After the container is up and running, and you've established a connection, you will observe a modification in your remote 
    environment status displayed at the bottom left of the Status bar.

    ![image](https://github.com/Sruti-sahini/Python/assets/100782959/5925a4a0-0571-4005-a946-36cd58664e8a)

**Check your environment** <br>
    A significant benefit of developing within a container is the ability to utilize precise versions of required dependencies for your 
    application, all without affecting your local development environment. <br>
    The dedicated container utilized in this guide includes Node.js version 18. You can confirm this by opening a new terminal through 
    the "Terminal" menu and selecting "New Terminal" (or using the shortcut Ctrl+Shift+`), then entering the following command: <br>
```    
    node --version; 
    npm --version;
```

This should show the following versions:

![image](https://github.com/Sruti-sahini/Python/assets/100782959/b7554227-74c1-45fc-9f8b-568bfdde90de)

- **Run the application** <br>
    Now, you can press the F5 key, initiating the execution of the application within the container. Once the process commences, navigate 
    to http://localhost:3000, and you should observe the basic Node.js server up and running!

    ![image](https://github.com/Sruti-sahini/Python/assets/100782959/20f18696-eebf-4fae-9f1e-38377cabe107)

 - **Ending your container connection** <br>
    To conclude your session within the container and return to running VS Code on your local system, simply select "File" and then 
    "Close Remote Connection."


