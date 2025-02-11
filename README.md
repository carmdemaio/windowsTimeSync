# windowsTimeSync
Syncs Windows System Time, to be run at startup

Place the timeSync.bat file in your windows startup folder. You can open it quickly by pressing Windows Key + R and running "shell:startup". Please note that some versions of Windows has a startup folder for individual users as well as for all system users. Individual startup folders are located somewhere within the user's folder. 

After you add the file to your startup folder, I would hit Windows Key + R and run msConfig. From there make sure that the bat file is set to run. Then restart your system. It may take 30 to 60 seconds for this bat file to run after a user logs on. 

If the system time does not automatically update after startup hit Windows Key + R and run services.msc Make sure that the local service Windows Time is set to Automatic startup type. To modify this, right click on Windows Time and select Properties. Reset your system again.

I wrote this file because I setup a dual boot between Ubuntu and Windows. Whenever I boot up Ubuntu, the system time gets converted to UTC which throws off the system time for Windows. Since websites' security certificates rely on system time to verify certificates I could not access most websites and the system time threw off how the Flux application worked. 
