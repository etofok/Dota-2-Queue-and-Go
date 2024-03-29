# Dota 2 Queue-And-Go

<img src="/icon.ico" width="150" alt="qng_icon">


# (!) IMPORTANT AND REQUIRED:

(!) Requires AutoHotkey v1.1 (not v2.0). 
Download here: https://www.autohotkey.com/

(!) MAKE SURE your 'ShareToChat.jpg' image IS THE SAME IMAGE as in your in-game lobby!

If you use a different resolution - just retake the image with 'PrintScreen', then crop it in 'Paint'.


## Quick Summary

Once upon a time there was a Dota 2 player who enjoyed the game. He really wanted to play multiple games in row, but he had a problem.

He ALSO wanted a fresh cup of coffee (and a bio break).

But waiting several minutes for the queue to pop, only for someone not to accept the 'Your Game is Ready'... is annoying.

Doing this all over again only to get back into the queue because of the players "has not connected"...

Yeah.

He really wanted his coffee.


**Dota 2 Queue-And-Go** helps players to successully queue and end up at the pick phase successfully, without macro spamming the client.

**Queue-And-Go** automatically accepts '*Ready check*' pop-ups, '*Game is Ready*' pop-ups and *deactivates itself* after everyone has connected.

It understands where your "Play Dota" button is, and it understands when to deactivate itself, so the ONLY user input is to launch.


The best thing: 

it only needs to 'see' this little tiny image on your screen - the 'Share to Chat' button, 

<img src="/resources/ShareToChat_placement.png" width="850" alt="qng_stc">

...which means the app works in **ANY** interface language,

for every game mode

AND in every screen resolution. 


# What's in the Package

- [x] an AutoHotkey file (.ahk) ---> Dota 2 Queue-n-Go.ahk, 
- [x] a tray icon (.ico) ---> icon.ico,
- [x] reference Image (.jpg) ---> ShareToChat.jpg for the 1920x1080 resolution


# How to Use

<img src="/resources/qng_foreground.png" width="850" alt="qng_foreground">

- Enable "Bring Dota to foreground on match found" in Options -> Advanced.
- Enable "Bring Dota to foreground for ready checks" in Options -> Advanced.
- Enable "Bring Dota to foreground for pick phase and game start" in Options -> Advanced.
- (!) MAKE SURE your 'ShareToChat.jpg' image IS THE SAME IMAGE as in your in-game lobby!
- Press [ALT + N] to activate the script.
You can change the hotkey using any text editor like Notepad.

<img src="/resources/qng_notepad.png" width="850" alt="qng_notepad">


# How it actually works

<img src="/resources/qng_logic.png" width="850" alt="qng_logic">

* The script locates the Play Dota button, which is consistently positioned approximately 5% from the right edge of the window and at a similar height to the ShareToChat.jpg image.
* The script queues for the game and minimizes the Dota 2 window.
* When the game is ready Dota 2 will be brought to the front as specified in the options
* The script then presses Enter once, assuming there's a button to be pressed since the Dota 2 window becomes active.
* After pressing Enter, the script minimizes Dota 2 again.
* After a short delay, Dota 2 will be brought forward again under the following conditions:
a) A new 'Game is Ready' pop-up appears due to someone failing to accept the game previously.
b) Everyone has successfully accepted the game and is loading into the pick phase.
* Last but not least, the script scans for the ShareToChat.jpg image every second for the next 30 seconds.
a) If the ShareToChat.jpg image IS NOT detected again, everyone has successfully connected.
b) If the ShareToChat.jpg image IS detected again, someone failed to connect, indicating a return to the main lobby screen and queuing for another game, prompting the script to minimize the Dota 2 window and wait for another game pop-up.


It was fun to make it.

etofok
