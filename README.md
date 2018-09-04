# raspivoice

1. install Raspbian Stretch Lite https://www.raspberrypi.org/downloads/raspbian/

2. update the OS (sudo apt-get update && sudo apt-get upgrade)

3. enable SSH (sudo systemctl enable ssh && sudo systemctl start ssh)

4. add the audio card (Raspiaudio MIC+ Sound Card https://www.raspiaudio.com/)

More about the card: https://www.raspiaudio.com/raspiaudio-aiy

5. test the card, as described here: 

6. install some useful tools:

sudo apt-get install nano git-core python-dev bison libasound2-dev libportaudio-dev python-pyaudio --yes

7. test audio playback, using one of these .wav files:

http://www.music.helsinki.fi/tmt/opetus/uusmedia/esim/index-e.html

for example:

wget http://www.music.helsinki.fi/tmt/opetus/uusmedia/esim/a2002011001-e02.wav

aplay a2002011001-e02.wav

At this point, you should be hearing some music!

8. install pip3

sudo apt-get install python3-pip

9. setup AIY packages (Google voice kit), then reboot: 

https://github.com/google/aiyprojects-raspbian/blob/aiyprojects/HACKING.md

10. continue installing Google Assistant packages

git clone https://github.com/google/aiyprojects-raspbian.git AIY-projects-python

sudo pip3 install -e AIY-projects-python/src

11. install numpy:

pip3 install numpy

12. install libf77blas.so.3:

sudo apt-get install libatlas-base-dev

13. test everything (record, playback):

python3 /home/pi/aiyprojects-raspbian/checkpoints/check_audio.py

14. install SpeechRecognition package, which supports several engines, both offline and online: https://pypi.org/project/SpeechRecognition/

pip3 install SpeechRecognition

15. install PyAudio: https://people.csail.mit.edu/hubert/pyaudio/

sudo apt-get install python-pyaudio python3-pyaudio

16. install FLAC conversion utility

sudo apt-get install flac

17. install SWIG:

sudo apt-get install swig

18. install PocketSphinx:

pip3 install --upgrade pocketsphinx

19. install Libpulse, or Sphinx won't compile:

sudo apt-get install libpulse-dev

20. install PocketSphonx for real:

pip3 install --upgrade pocketsphinx



