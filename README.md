# MediaPipe-Hands-OSC
MediaPipe-Hands-OSC implements the Google MediaPipe Hand model on the browser, getting the landmarks from two hands and outputting to OSC via UDP using the [osc.js library](https://github.com/adzialocha/osc-js#osc-js).  
MediaPipe-Hands-OSC 使用浏览器运行 Google MediaPipe 的手部识别模型，识别坐标数据后通过 OSC 发送。  

# Installation Guide for Beginners 小白使用指南
You must have Node installed on your computer. If you don't, download the latest stable version [here](https://nodejs.org/en/). Launch the installer and install Node.  
安装node.js，[点击这里](https://nodejs.org/en/)安装  

Download the MediaPipe-Hands-OSC code folder.  
下载这个库  

Open your terminal window on Mac (press CMD + spacebar simultaneously, in the search window, type in terminal and enter) or Command Prompt on Windows. Go to the folder where you downloaded MediaPipe-Hands-OSC. You can do this by just dragging the folder into the terminal winwdow and press enter. Or type in 'cd' followed by the path name. For example, if you put the folder on your desktop:  
在 Mac 上打开终端窗口(同时按 CMD + 空格键，在搜索窗口中键入终端并输入)或 Windows 上的命令提示符。转到 MediaPipeHandsOSC 的文件夹。您可以通过将文件夹拖动到终端窗口并按 Enter 来完成此操作。或者键入“ cd”，后跟路径名。例如，如果你把文件夹放在桌面上:  

```$ cd desktop/MediaPipe-Hands-OSC-main/```

Install package dependencies (the files you will need to run the code) by typing in:  
输入下面的命令安装运行依赖项(运行代码所需的文件)

```$ npm install```

Mac users - If you get a permission error, try typing this instead and when terminal asks for a password, enter your administrator password:  
Mac用户--如果你遇到权限错误，输入下面的命令提升权限，当终端要求输入密码时，输入你的管理员密码  

```$ sudo npm install```

Then, run bridge.js to start the OSC link by typing:  
然后，输入下面的命令运行服务  

```$ node bridge.js```

You should see a message 'osc success'.

Double click to open the index.html file OR go to https://monlim.github.io/MediaPipe-Hands-OSC/ on your browser. Start waving your hands around.  
双击打开index.html文件或进入浏览器的https://monlim.github.io/MediaPipe-Hands-OSC/ 就可以开始挥舞双手了。  

# Usage
Please use Google Chrome or Firefox on a Desktop. Will not work in Safari. UDP send on port 8080 and receive on port 9129.  
请使用谷歌浏览器或火狐浏览器。在Safari浏览器中不能正常工作。UDP发送端口为8080，接收端口为9129。

Note: you will need another application to receive your OSC landmarks and process them. There is a MaxMSP patch example in the assets folder. Landmarks are prefixed as:

* /lx for Left Hand x-axis 
* /ly for Left Hand y-axis
* /rx for Right Hand x-axis
* /ry for Right Hand y-axis

This is a list of the landmarks (image provided by Google MediaPipe):

![Image provided by Google MediaPipe](https://monlim.github.io/MediaPipe-Hands-OSC/assets/Mediapipe_Hand_landmarks.png)

For more information on the hand-tracking model, please see [MediaPipe documentation](https://google.github.io/mediapipe/solutions/hands.html).
