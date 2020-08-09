# cncjs-pendant-boilerplate-pause-resume-buttons
This is a modification of the boilerplate api code, to allow the use of physical buttons for pause and resume of your CNCjs. 


# Requirements:
1. CNCjs is installed and working on a raspberry pi (this is tested on a raspberry pi 3b+)
2. wires and buttons
3. cncjs-pendant-boilerplate is installed on raspberry pi

# Checklist (short install instructions)
1. download cncjs-pendant-boilerplate to a new folder with wget, unzip it, cd into the folder

https://github.com/cncjs/cncjs-pendant-boilerplate/archive/master.zip


2. install cncjs-pendant-boilerplate with this command -> npm install
3. install onoff module with this command -> npm install onoff
4. modify bin/cncjs-pendant-boilerplate with contents in this repository
5. run the file with ./bin/cncjs-pendant-boilerplate
6. hook up buttons to 5v on one side and then the pin 11(pause) or 17(resume) on the other end of the wire.
7. when buttons are pressed you will see output in the console
8. create a service that launches the file on reboot.

# More automated version
```
mkdir pendant
wget https://github.com/cncjs/cncjs-pendant-boilerplate/archive/master.zip
unzip master.zip
cd cncjs-pendant-boilerplate
npm install
npm install onoff
cd bin
rm cncjs-pendant-boilerplate
wget https://raw.githubusercontent.com/kylecop/cncjs-pendant-boilerplate-pause-resume-buttons/master/cncjs-pendant-boilerplate
```
