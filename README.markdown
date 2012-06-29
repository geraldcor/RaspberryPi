# Raspbery Pi Scripts and Tinkerings

This is a base repository for all of the scripts and software I create for the [Raspberry Pi](http://www.raspberrypi.org, "Raspberry Pi Website")

## Contents Thus Far

### startup_mailer.py

This is a script that when configured correctly, and when the raspberry pi is configured correctly, will email you the ip of your raspberry pi on startup so that you can easily run the pi headless and obtain the ip for SSH reasons.

#### Usage

 * Copy the script to a directory on your pi.
 * Edit the script and change the 3 lines pertaining to your email credentials and where you want the email sent.
  * If you don't have a gmail account, get one and make your life easier, or else edit the smtp stuff as needed.
 * Make the script executable
  * `sudo chmod +x startup_mailer.py`
 * Edit your `/boot/boot.rc` file using nano and add the following at the bottom of the file.
  * `#Script to email ip address upon reboot. Change the path to where you saved the script
	python /home/pi/Code/startup_mailer.py`
  * If you don't have `/boot/boot.rc` see [this wiki entry](http://elinux.org/RPi_Advanced_Setup, "Raspberry Pi Wiki") for more info.
  * Basically all you have to do is rename `/boot/boot_enable_ssh.rc` to `/boot/boot.rc`
 * That's it. Reboot and you should get an email


