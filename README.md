autologin-on-boot
=================

Provides autologin and starting X-server on boot (once per boot). This means: For every boot, there is ONE autologin and ONE autostarted X-Server. For example, when X crashes, there is no X-restart-loop.

To set the autologin user, simply execute /bin/autologin-on-boot (as root) and enter the username. To disable autologin, call autologin-on-boot again and leave the username blank.

The username is stored in /etc/autologin-on-boot.conf. The name needs to be in the first(!) line. If the line is empty or the file is missing, autologin is disabled.

If you wish to execute another application as "startx" or want to skip it, simply modify the file /etc/autologin-on-boot.profile and replace the line containing startx with an other command.

Dependencies: systemd, xorg-server.

autologin-on-boot works only with systemd (in the moment).
