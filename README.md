# How to use the ASClab server

The mechanical specifications of the ASClab server is:  
- AMD Threadripper pro 9975ws
- NVIDIA RTX 6000 Blackwell
- 2X NVIDIA RTX 3090

This workstation has **144GB** of vram, with Ubuntu 24 installed.


## How to access (Headless)

Accessing the server headless is really simple. First connect to the lab wifi:  
**TP-Link_3F91**  

Make sure your PC is connected to the wifi above, not RPI network. Then you can simply use windows powershell(Windoes) / command terminal(Ubuntu) to

```bash
ssh asclab_pub@192.168.0.4
```

You will be asked to provide password. You can ask the server admin for the password. Note that this is the headless way of accessing the server, and you should run your code without any interfaces like VScode.

### Copying to Server Storage
You can copy your local files to the server using scp.
```bash
scp ./your/folder/name asclab_pub@192.168.0.4:/home/asclab_pub/projects/path/to/your/folder
```

## How to access (VSCode)
In Visual Studio code, accessing the server is convenient. First you need to install  
- Visual Studio Code
- Remote - SSH extension

After you have installed all these necessary stuff, you can navigate to _Remote Explorer_ tab on the left-top corner, and choose _Remotes (Tunnels/SSH)_ from the drop down menu on the right of the _REMOTE EXPLORER_.  

Now, you can add the SSH Connection Command:

```bash
ssh asclab_pub@192.168.0.4
```

You will be asked to provide password. You can ask the server admin for the password. Select:

```bash
C:\Users\your_name\.ssh\config
```

for the file to update. Now you can always connect to the server using VS Code.
