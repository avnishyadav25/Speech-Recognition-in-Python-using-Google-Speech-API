# Speech-Recognition-in-Python-using-Google-Speech-API

Speech Recognition is an important feature in several applications used such as home automation, artificial intelligence, etc. This project aims to provide an introduction on how to make use of the SpeechRecognition library of Python. This is useful as it can be used on microcontrollers such as Raspberri Pis with the help of an external microphone.

---

## Required Installations

The following must be installed:

**Python Speech Recognition module:**
```
 sudo pip install SpeechRecognition
```
**PyAudio: Use the following command for linux users**
```
sudo apt-get install python-pyaudio python3-pyaudio
```
***If the versions in the repositories are too old, install pyaudio using the following command***
```
sudo apt-get install portaudio19-dev python-all-dev python3-all-dev && 
sudo pip install pyaudio
```
Use pip3 instead of pip for python3.

**Windows users can install pyaudio by executing the following command in a terminal**
```
pip install pyaudio
```

---
### Speech Input Using a Microphone and Translation of Speech to Text

**Configure Microphone (For external microphones):** It is advisable to specify the microphone during the program to avoid any glitches.
Type `lsusb` in the terminal. A list of connected devices will show up. The microphone name would look like this
```
USB Device 0x46d:0x825: Audio (hw:1, 0)
```
*Make a note of this as it will be used in the program.*

**Set Chunk Size:** This basically involved specifying how many bytes of data we want to read at once. Typically, this value is specified in powers of 2 such as 1024 or 2048

**Set Sampling Rate:** Sampling rate defines how often values are recorded for processing

**Set Device ID to the selected microphone:** In this step, we specify the device ID of the microphone that we wish to use in order to avoid ambiguity in case there are multiple microphones. This also helps debug, in the sense that, while running the program, we will know whether the specified microphone is being recognized. During the program, we specify a parameter device_id. The program will say that device_id could not be found if the microphone is not recognized.


**Speech to text translation:** This is done with the help of Google Speech Recognition. This requires an active internet connection to work. However, there are certain offline Recognition systems such as PocketSphinx, but have a very rigorous installation process that requires several dependencies. Google Speech Recognition is one of the easiest to use.

---
