# Linux Matlab Installation

```sh
I had the same issue but I fixed doing these:

Extract R2016b_glnxa64_dvd1.iso to ~/MATLAB

Extract R2016b_glnxa64_dvd2.iso to ~/MATLAB2

Copy all files from MATLAB2 to MATLAB (merging), including the hidden file .dvd2

Call the install script inside of ~/MATLAB

And, don't forget to check the directory permission
```


```sh
After toying around with the activation client I finally have a good answer as to why MATLAB will not activate. Here are the steps to getting everything working!! This is also assuming that you have MATLAB installed and cannot get it to launch.

Quick questions to ask yourself

Did I launch the installer as root?
Where did I install MATLAB?
If you installed as root (which you should have) then your fine. If not uninstall and install as root.

Ok! Lets get to it!

cd to into where you installed MATLAB For me it was the default that was given but you may have wanted to install it in a different location.

Default install location: /usr/local/MATLAB/R(year)(a or b)

Now you can list everything that is in that directory by typing ls into the terminal window.

Now type cd once more by typing cd bin (this is where the activation client is stored)

Type in the terminal

sudo ./activate_matlab.sh
Now a window will pop up just like it did when you were installing it. This time you need check the bubble in front of "Activate manually without the Internet."

Now check the bubble in front of "I do not have a license file. Help me with the next steps."

Here you will find your computers basic install info. This was just to check what your computer login name was and to make sure it is root.

Now go back to the beginning of the activation client menu and fill in the bubble that says "Activate automatically using the Internet."

Do everything you did before except this time at the end of the activation when it asks you to type in the name of your computers user, you need to type root, instead of your username or instead of anything you want to put.

Optional: if you haven't already done it, you can install matlab-support so you can launch it after you finish activating MATLAB. You can do this by typing

sudo apt-get install matlab-support
I hope this helps! GOOOD LUCK!
```
