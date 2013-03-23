# ownCloud mobile apps


## General thoughts

* Generally the design of the mobile apps should be very simple. There’s not much to it and the focus should be on the files. Hence it’s also possible to keep the design largely similar for iOS and Android (using the interface elements of the respective platform of course)
* Offline should not be handled like an exception. People are often offline, be it because they have only wifi plans, or are on a plane, or just because the connection is bad. Creating folders and uploading files should just work, the changes can be synced once online again. Inaccessible files (not starred or saved offline) should be greyed out in the document list and not clickable.
* Identity, especially app icon, splash screen and logo on Setup dialog: better keep in line with the web interface (and more elegant look) and have dark blue background (#1d2d42) with a white ownCloud logo (and a subtle fade, like on the [GitHub organization avatar](https://github.com/owncloud/)?


## Layout

There are 5 general views:

* **File & folder list**
  * top bar
     * menu button to the left
     * current folder title in the middle (»ownCloud« when in root folder)
     * add button on the right: on click shows popover with buttons »Upload Here« and »Create Folder« (see Dropbox), clicking outside the popover will close it
     * (no use of Android dropdown or multiselect button)
  * no bottom bar needed
  * listing files and folders like already now
  * sorted alphabetically, folders and files mixed (toggle to sort by modified date would be great, see Dropbox)
  * alphabetic dividers should appear only if there are more than 15 elements in the current folder
  * document count shown as last entry in list in the fashion of »3 folders & 5 files, 180 MB« (see iOS Photos)
  * star/offline indicator should not take a whole column, just be a triangular badge (see Pocket iOS app)
  * ideally show file thumbnails for easier recognition (see Dropbox)

* **File view**
  * detail view of a file
  * focus on content, top and bottom bars are half-transparent and vanish after a while, and toggle visibility on tapping the file
  * top bar: back function, and document title
  * bottom bar (for easier finger access), all icons monochrome
     * Share
     * Star (outline when not starred, shape when starred)
     * then maybe »open with« or »delete«
  * swiping left/right will cycle through files in that folder (like iOS Photos), except when zoomed in of course where swiping pans the file

* **Menu**
  * the menu moves in from the left on clicking the menu button or swiping from the far left / screen edge, moving the content area to the right. Always showing a bit of the content area still on the right, as indicator and allowing for a quick swipe to go back. (see Gmail on iOS and lots of other apps)
  * Entries:
     * Files
     * Shared
     * Favorites
     * Uploads
     * Settings (at the bottom, see next point)
  * current entry is highlighted

* **Settings**
  * account list, directly on that page (basically like now the list on the »Manage Accounts« page, but not on a separate page)
     * icon showing connection status
     * tapping an account will switch to that one, automatically switching to the »Files« view
     * swiping to the left on an account row will show a »Disconnect« button to remove the account, much like »Delete« for files
     * each account row has an arrow on the right, tapping will open the connection details to change them (looking just like the Setup dialog
     * last entry in the list is »Add account« (which will open a new Setup dialog, see next point)
  * PIN
  * wifi upload settings
  * storage limits info
  * version number
  * link to ownCloud website

* **Setup dialog**
  * keep it simple
     * ownCloud logo
     * »Connect to your ownCloud«
     * »Server http://« field
     * »Username« field
     * »Password« field (with show password eye toggle, only shown when at least one character is entered)
     * »Connect« button on the bottom right
  * for the behavior, refer to the [desktop client setup dialog](https://github.com/owncloud/mockups/blob/master/desktop/README.md#setup) (excluding the Advanced section)
  * the fields should use in-field labels to reduce visual content, like in the web interface. The labels should not vanish on click but only as soon as something is typed into them (see web interface, or GitHub Issues iOS app)
  * the fields should be visually grouped, like in the web interface (also see GitHub Issues iOS app)
  * as soon as a field is clicked for entry, the page will move up to the field set so the software keyboard does not obstruct the fields or the connect button. People should not need to manually scroll here.


## Actions

* **open** file/folder: simple tap. Any downloaded document will, in addition to open a document and save it for offline access
* **menu** (sidebar): menu button on the top left, or swipe from far left (edge of the screen). When in a subfolder, the button on the top left will change to 1-level-up, and the swipe from far left gesture will still enable people to quickly access the other menu entries. Changing menu entries will preserve the location in the other menu entries (in case you were in a deep folder or had a file open), clicking the currently selected menu entry will go to the root folder of that entry.
* **star** or **share** a file: inside the open document there will be icons to star/share in the bottom bar
* **rename** file/folder: for folders, clicking on the folder name in the title will go into rename mode (see iA Writer). For files, clicking on the file name in the file view will do the same.
* **delete** file/folder: swipe from right in the document list will show a red »Delete« button (classic pattern). For files which are already downloaded, there will be a dialog asking »Only delete local file« (grey), »Delete from server« (red), »Cancel« (dark grey). (See iBooks for reference)
* (if needed) **multiselect**: swipe from left, will move the entries slightly to the right (in accordance with the gesture) and reveal checkboxes
* **move** files/folders: tap & hold, will make the tapped entry movable. Similar to rearranging apps on the iOS home screen, also used by iA Writer)
* **search** files/folders: pull down the file/folder list a bit to reveal the search bar (list is scrolled down a bit to not show the search bar by default, common pattern)
* **refresh**: pull down the list more (common pattern)
* **undo**: shake (this is an established pattern, see iOS Notes)

