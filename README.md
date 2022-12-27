# urepl
Micropython UDP REPL like communication


urepl or 'how I got too impatient to wait for webrepl on the rp2040 w'

Redirecting STDOUT is difficult on the ESP32 with micropython. The easiest solution to get something similar is to create a print function that executes the commands recursively until nothing is left to run. If the code contains a call to frint() the internal 'replacement' for STDOUT to then send via UDP to a client device.

Mostly written as a challenge or proof of concept.

Ends up helping UDP socket communication by automagically grabbing ip addresses when possible.
