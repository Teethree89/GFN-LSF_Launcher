# GFN-LSF_Launcher
A small launcher (MACOS only) that automates turning off location services, enabling firewall, opening and waiting for GFN to close to then revert those changes.

Real simple install, download the files anywhere, and do the following:

Install Homebrew (Open a terminal and paste one of these at a time):

1. /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
2. brew install switchaudio-osx.

Set your launchers permissions:

1. Open your System Preferences > Privacy & Security > Accessibility
2. Press the + Button and add in the Launcher Application from the files you downloaded, it will have the red Nvidia Icon.

Set your password:

1. Inside your files you will see a txt file called password.txt
2. paste your case sensitive password in it, the scripts use it for text input

Double click the red Nvidia Launcher Application, the following will happen:

1. The MacOS voice will tell you its turning off location services
2. System setting will open and navigate to location services
3. A password prompt will appear and autofill
4. services will turn off
5. firewall (voice prompt too) will turn on
6. GeForce Now will turn on
7. A voice prompt will tell you that its waiting for GFN to close
8. If at this point you turn on your bluetooth headset, and your default mic changes (but you don't want that) 
you will hear it set your "system microphone to macbook air internal" which can be edited in the "Launcher" scrip
just set micChek to false on line 2, or edit it below as needed with SwitchAudioSource etc
9. When you close GFN the settings will revert (except for headset, just turn it off)
