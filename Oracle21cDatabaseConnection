# Connection Problems with Oracle 21c Database<br><br>

## Solution for Windows Based Systems<br><br>

The Windows based system uses a config file to configure both the Listener service and the TNS service.<br>
By default, these use the local machine's network IP address. This will cause a problem when you move to a new network and your IP address changes.<br><br>

To solve this problem, we instead configure the database to reference your computer's Device Name (aka NetBIOS name).<br><br>

1. Press the Windows key + X, then select "System" from the popup menu.<br><br>

!{Windows key + X](URL)<br><br>

2. Note (highlight, and ctrl + c) the "Device Name" noted in the "Device specifications" section.

![Device Name](URL)<br><br>

3. Open a Windows Explorer window and navigate to the folder "C:\app\*{your windows login name}*\product\21c\homes\OraDB21Home1\network\admin"

![Folder](URL)

4. Open the "listener.ora" file using Notepad (right-click > open with) to edit it.<br><br>

5: Under the "LISTENER" key, change the "HOST" value to the Device Name you copied in step 2, as highlighted blue in the image below.

![Listener.ora](URL)

Then save the file and close notepad.

6. In the same folder, open the "tnsnames.ora" file using Notepad (right-click > open with) to edit it.<br><br>

7. Under the "XE" key, again change the "HOST" entry to the device name copied in step 2. <br>
Then, under the "LISTENER_XE" key, also change the "HOST" entry to the Device Name copied in step 2, as highlighted blue in the image below.<BR><BR>

![Tnsnames.ora}(URL)

Then save and close the file.

8. Reboot the computer - this is sadly essential.

9. You should now be able to connect to your database using the details shown below, using the password you set at installation.

![Connect](URL)


Cheers pal. :)


