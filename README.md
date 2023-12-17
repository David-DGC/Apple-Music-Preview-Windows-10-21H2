# Apple Music Preview for Windows 10
The Windows 11 exclusive Apple Music Preview app running on Windows 10 21H2!

![image](https://github.com/kuba03099/Apple-Music-Preview-Windows-10-21H2/assets/152105133/1ad7c28c-561e-48e5-a12a-534ff6cfc897)


# What does this do?
This is an installer for the new Apple Music Client. It's supposed to be exclusive to Windows 11.

(And yes, lossless and music downloads work fine. The actual app isn't modified in any way other than the AppxManifest to allow it to run on older versions of Windows.)

Windows 11 is just a skin on top of Windows 10, with some extra bloat. So the overall actual system is nearly identical, just Windows 11 is buggier and more bloated with spyware. Funny, ain't it? So Apple Music can run on Windows 10 21H2 just fine. 

# Installation Instructions

1. Go to the **releases** page, and there will be a .zip containing all of the files needed to install this. Download that file.
2. Go to Settings > Update and Security > For Developers, and enable "Install apps from any source, including loose files."

![image](https://user-images.githubusercontent.com/70412932/235552873-139b9832-d1ef-4e0a-b090-48b2670d0281.png)
Just like in this image.

3. Now open and extract the zip file.
4. Right click the **Installer.bat** file, and run it as administrator!

You may see some errors in red, don't panic! These are usually because the dependencies the script is trying to install are already on your system or are there is a newer version installed.

If you encounter any issues, refer to the steps below. :)

# Troubleshooting
Issue 1: Sometimes the Apple Music icon doesn't show in the Start Menu or anywhere, and manually double-clicking the .exe in the Documents folder shows an error like this.

![image](https://github.com/kuba03099/Apple-Music-Preview-Windows-10-21H2/assets/152105133/f9c11ade-e4ba-45de-bb75-fb6f1deb8873)

To fix this, delete the "AppleMusicClient" folder in Documents completely and run the script as admin again, this usually fixes this.


Issue 2: Sometimes there may be UWP apps running or services that are running that the script cannot stop. A simple way to fix this is to go into Task Manager and go to the "Startup" tab. And disable everything, then reboot.

![image](https://user-images.githubusercontent.com/70412932/235554700-0de40509-0670-4a95-9e83-433de4da9c3a.png)

You can re-enable these after you're done installing.

# How to upgrade to the latest version if there is a new release
To upgrade Apple Music, wait for a new release with the latest version to drop. Before installing, uninstall the previous version and go to your Documents and delete the previous version's "AppleMusicClient" folder. Then just follow the installation instructions for the latest version.

# If a new release hasn't been released or the project doesn't get maintained anymore
Download the last release available and extract it. Delete all the contents inside of the "AppleMusic" folder, but don't delete the folder itself.

Then you'll need to download a ".msixbundle" file from a source like [https://store.rg-adguard.net/](https://store.rg-adguard.net/)

1. Copy and paste the app's URL in the search bar ([https://www.microsoft.com/store/apps/9PFHDD62MXS1](https://www.microsoft.com/store/apps/9PFHDD62MXS1)).
2. Select "Retail" instead of "RP" in the search bar.

    ![image](https://user-images.githubusercontent.com/70412932/235558728-63d97d11-1988-41d7-a0ec-b8e10c1259bc.png)

3. Select the one with the ".msixbundle" file name extension.

    ![image](https://user-images.githubusercontent.com/70412932/235559192-29a23191-0dc0-49ec-8c78-52c63ec319ce.png)

4. Extract the file with an utility like [7zip](https://www.7-zip.org/download.html).

    ![image](https://user-images.githubusercontent.com/70412932/235559495-6cf077c3-f782-43af-a96a-7f5b7632f8aa.png)

5. Enter the folder and extract the ".msix" file.

    ![image](https://user-images.githubusercontent.com/70412932/235559659-c7f49171-6677-47a9-855d-896dbdde0cda.png)

6. Copy the contents inside this extracted folder to the "AppleMusic" folder you just emptied out.

7. Then in that folder where you just copied those files, find and delete the "AppxMetadata" folder and the "AppxSignature.p7x" and "AppxBlockMap" files.
   
![image](https://github.com/kuba03099/Apple-Music-Preview-Windows-10-21H2/assets/152105133/25a6da91-37e7-4ddd-8641-df435cdd0577)


8. Then find the "AppxManifest" file. Open it in an app like Notepad++ or just regular Notepad and find **MinVersion="XX.X.XXXXX.X"**. Replace that with **MinVersion="10.0.19041.0"** and save the file.

Here's an example of how it should look like now:

![image](https://github.com/kuba03099/Apple-Music-Preview-Windows-10-21H2/assets/152105133/9ad07d9b-375a-45e9-b3a2-66db2cc76719)


9. Follow the installation instructions, and that's it! (Before installing, uninstall the previous version in Settings and go to your Documents and delete the previous version's "AppleMusicClient" folder.)

# How to uninstall
Uninstall Apple Music like any other Microsoft Store app, by going to **Settings > Apps > Apple Music Preview > Uninstall**, then just go to your Documents and delete the previous version's "AppleMusicClient" folder and that's it, uninstalled!

# Known issues 
None that I know of :D. At least none that aren't in the app itself. They can be replicated on Windows 11 as well.

# Notes
- This has not been tested on any Windows 10 version from before 21H2. But it *should* work just fine. As the system files from 2004 and beyond are the same.

