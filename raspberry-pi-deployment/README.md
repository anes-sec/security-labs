# Raspberry pi deployment

## What it is
Raspberry Pi deployed on my own home network, configured it to run Nessus for vulnerability scanning my network.

## What I did
-Installed Raspberrypi OS on the Pi computer
-Connected it to my home network
-Attempted ton install and configre Nessus for vulnerability scanning on the device
-Ran into a specific compatibility error when trying to run scans
-Switched the OS from 64-bit to 32-bit as doing research led me to this being one of the probable issues in which it was not
-Spent weeks trouble shooting through various approaches before identifying a likely root cause

## What I found / learned
-Tracked the issue down to a hardware compatibility gap being: Tenables official documentation lists Nessus support for the Raspberry Pi 4 Model B (8GB RAM minimum) - the Raspberry Pi 5 isn't listed as a supported configuration, which most likely explains the persistent error despite extensive troubleshooting
-Learned to check a vendors official hardware compatibility list before attempting a deployment, compared to just assuming the newer hardware is automatically supported
-Also learned that switching from 32-bit to 64-bit OS was not the right pick - Nessus typically expects 64-bit, in which wasn't the correct troubleshooting path
-If I were to do this all from scratch again, I would either source a Raspberry Pi 4 model B, or explore other scanning tools (like OpenVAS) that may not carry the same type of hardware restriction


## Tools used
Raspberry Pi 5, Raspberry Pi OS, Nessus (failed)

## Status
Unresolved due to the hardware compatibility, documented as a troubleshooting case study, still being worked on currently.
