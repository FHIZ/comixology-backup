Comixology Backup
======

Do you like [Comixology](http://comixology.com)? Me too!

Are you annoyed that you can't download the comics you bought in a standard format, readable by all possible software? Me too!

This is a Chrome/Chromium extension, that allows you to do just that. It should work on any OS where Chrome works.

*IMPORTANT:* Do not use the extension for piracy! Only create private backups! We do not intent to compromise ComiXology. **Downloaded comics always have your username included. Distributed comics can be tracked back to you!**

Installation
-----

The installation is slightly complicated (since I don't want to add this to the Chrome Store). 
There are two ways of installing the extension.

### First possibility

The first way is [by this help page](https://support.google.com/chrome_webstore/answer/2664769?hl=en)

- In Chrome, click on the settings icon on the right (looks like three vertical lines on top of each other)
- Select Tools > Extensions
- **Drag and drop** the CRX file **from your disk** to the extension page
- Now you just open your comics in the Comixology reader and you should see an orange panel, asking for back-up.

### Second possibility

The second way is without drag-and-drop.

- In Chrome, click on the settings icon on the right (looks like three vertical lines on top of each other)
- Select Tools > Extensions
- Select "Developer mode"
- Click on "Load unpacked extension"
- Select the "source" folder
- Now you just open your comics in the Comixology reader and you should see an orange panel, asking for back-up.

Updates
-----

If you want to be notified about updates you can add an update server in the extensions options. You get there by opening the extensions panel in the settings and then click on "Options" right to the Comixology Backup extension. The options should open and you can click on "Set update server".

The update server URL is: `https://raw.githubusercontent.com/Cortys/comixology-backup/master`

Copy it exactly like that.

### Why it's not on Chrome Store?

I am fairly certain Comixology will, unfortunately, try to remove this extension from Chrome Store, because it goes around their DRM.

How to use
-----

* Open a ComiXology comic (with at least two pages) in the web reader. An orange bar should appear, asking you if you want to backup.
* Click "Yes". Because this is the first time you use the extension a scan has to be created. This basically means that the extension will ask you to click on some element of the reader. The things you are asked to do (switch view mode, open thumbnails...) are operations you can accomplish with one click. So only perform ONE click in each step or the setup won't work.
* If everything worked fine you will get a success message and may start to backup your comic library now.
* Sometimes backups of comics with many pages (~200+) fail. To circumvent that you can enable *single image* container compression in the options and all the pages of the comic will be downloaded as separate images. To get a CBZ you then have to zip the images manually.

How it works
-----
You can look at the source code - but basically, it fetches the pixels of the canvas elements that compose to the opened page, puts them together, and then it downloads those again and zips them using zip.js.

About, licence
----

Project started by SpergLord Enterprises, LLC and continued by other awesome contributors.

If you have problems with the software/have an idea, add an issue on Github via Issues.

The code is under GPLv3 licence. Code uses JSZip by Stuart Knightley.
