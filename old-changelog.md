# Changelog pre 2017
_Prior to the github project to get Lazarus working on Firefox v52 and newer._

## 2.3 ##

* Removed show onupdate page as a workaround for a particular Firefox 4 bug

## 2.2 ##

* Multiple language support (thanks <a href="http://www.babelzilla.org">babelzilla</a>)
* Stop using jar files (Firefox 4 prefers normal directory structures within addons)
* bugfix: Legacy support for Firefox 3.0.x users 

## 2.1.1 ##

 * Legacy code removed to apply with stricter AMO reviews 

## 2.1 ##

 * Make compatible with Firefox 4.0beta9
 * Added workaround for compatibilty bug that caused a hang if Firebug was running whilst we attempted to run code in a background thread.
 * Replacing encryption components with javascript based encryption (not as fast but at least it works on all platforms)
 * Replace credit card numbers option 
 * Possible fix for the unresponsive script error at startup problem
 * Add idle observer to clean the database once per day after 5 minutes of inactivity 
 * Show a "saving form" icon in the statusbar whenever a form is saved
 * Set default form expiry time to 4 weeks
 * Css fix for remove forms textbox and dropdown
 * Look for key generation errors and notify the user if there is an error.
 * Don't require a password to delete the database (if database has become corrupted, then password will not work)
 * Bugfix: resetting password reports a key generation error even if the password reset works.
 * Remove all background threaded code (Firefox 4 really doesn't like them)
 
## 2.0.5 ##

 * Added info about the database on the options > database tab
 * Added button to clean (Vaccuum) the database  (options > database > Clean The Database)
 * Automatically backup the database on browser load (and option to disable backup)
 * New Crypto components fromo the Mozilla Weave team.
 * Zotero compatibilty problem
 * Fixed a couple of memory leaks reported by <a href="https://addons.mozilla.org/thunderbird/addon/2490">Leak Monitor</a>
 * Re-enabled options dialog resizing for windows and linux users
 * Require the Lazarus password to delete the database or delete saved forms

## 2.0.4 ##

 * Full text searching now enabled for other form elements (textboxes, input boxes, wysiwyg ...)
 * Ability to restore text to clipboard from an entire form rather than just a textbox.
 * Added "Remove All Saved Forms" button to database options 
 * Added "Delete Database" button to database options, to deal with corrupt databases.
 * Added an option to enable Lazarus in Private Browsing Mode.
 * Fixed a particularly difficult bug that incorrectly sized the options dialog 
 * Removed the welcome page from the options dialog

## 2.0.3 ##
 
 * Fixed: Editor text shouldn't be saved in private browsing mode
 * Added an option to hide the context menu icons
 * Lazarus Search: automatically close the window on a successful copy to clipboard operation.
 * Removed the "Unable to convert url to uri" error 
 
## 2.0.2 ##
 
 * More updates to the crypto component
 * Make compatible with Firefox 3.5 (beta 4)

## 2.0.1 ##

 * Updated crypto components to work on 64 bit Linux operating systems

## 2.0 ##

 * New Hybrid Encryption!. Using 2048 bit RSA and 256 bit AES encryption to secure your data. 
 * Password no longer needed for saving forms (only required when recovering forms) 
 * Now saves contents of textareas and WYSIWYG editors
 * New Text Manager: allows recovery of text data even if original form is no longer accessable.
 * bugfix: unresponsive script error when recovering selectboxes with large (10,000+) amounts of options
 * Removed obsolete update check
 
## 1.0.5 ##

 * Allow Lazarus to be disabled on a per site basis (right click on statusbar icon)
 * bugfix: Conflict with the <a href="http://www.feedly.com/" rel="nofollow">feedly</a> add-on.
 * bugfix: off by one date formatting error
 * Compatibility checks for Firefox 3.1 (beta 2)

## 1.0.4 ##

 * Rewrite the "should create new autosave point" code
 * Removing "check for updates" options (Mozilla policy prohibits downloading updates from anywhere but addons.mozilla.org)
 * Use window.open() instead of window.openDialog() to open the options dialog (dialog has no chrome in Fx for Mac)
 * bugfix: options dialog content hidden on for Fx3 on a Mac

## 1.0.3 ##

 * Added check for updates, and new update available statusbar icons.
 
## 1.0.2.2 ##
 
 * Fixed "Fails to restore forms containing unicode characters" due to bug in Firefox's base64 encode function "btoa" (<a href="https://bugzilla.mozilla.org/show_bug.cgi?id=439711">bugzilla #439711</a>).
 * Only ask to initialize the Software Security Device once, rather than once at every browser start.
 
## 1.0.2.1 ##
 
 * Removed incomplete locale files that should not have been included

## 1.0.2 ##

 * Fixed "Clear Private Data Now button doesn't clear forms even if checkbox is selected"
 * Fixed "Forms are not removed if both Clear Private Data on shutdown and Ask Before Clearing Private Data are selected"
 * Specified color of text in notification bar (text was not visible when using some themes eg pitchdark)
 * Use locale specific width and height for dialogs
 * Remove persistant window dimentions to help with translations
 * Incorrect selectbox elements were restored if the selectbox has additional entries added between save and restore.
 * Removed unused file from locale folder
 * Disable Lazarus if the Software Security Device has not been initialized 
 * Fixed a problem when an invalid version string was found in about:config that prevent Lazarus from initializing 
 * Initial state of context menuitems should be hidden until Lazarus is initalized
 * Prevented Lazarus from saving forms on html pages found in chrome urls.
 * Disabled "Master Password Required" notifications for search forms
 * Better updating of statusbar icon.
 
## 1.0.1 ##

 * Rework the form identifier to allow for the same form on multiple pages and restore forms across subdomains
 * Using notification bar instead of dialog if user hasn't yet logged into Firefox's Software Security Device
 * Update the statusbar icon after setting/unsetting the master password
 * Workaround for delay when right clicking on a form containing large amounts (30+ <abbr title="kilobytes">KB</abbr>) of data
 * Tidied links on the about dialog 
 * Added a more descriptive tooltip to the statusbar icon
 * Added a menuitem link to the online <abbr title="Frequently Asked Questions">FAQ</abbr>
 * Rearranged the folder structure to make it more compatable with babelzilla.
 * Using new <a href="http://developer.mozilla.org/en/docs/nsIJSON">Firefox 3 nsIJSON interface</a> (when available) for faster more robust encoding.
 * Add image to donate submenu item
 * Disable oninstall and onupdate pages for now.
 * Fixed a bug where the context menu is not reset if you right click off a form after right clicking on a form
 * Disable the restore form context menu item (rather than hiding it) if there is only one saved form and it is identical to the current form

## 1.0.0 ##
 
 * First Public Release (Wahoo!)
 * Autosave forms even if they contain no textual elements (eg, multichoice surveys)
 * Autosave forms if a user accidentally hits a reset button
 * Fixed a bug that prevented Lazarus from locating forms on some malformed pages
 
## 0.9.9 ##

 * Fixed a bug that prevented some forms from being saved when submitted
 * Cut down the number of autosaves shown in the submenu
 * Tweaked tooltip text in submenus

## 0.9.8 ##

 * Fixed a bug in the update process
 * Encrypt formIDs (previous version had the domain name as part of the ID, constituting a privacy issue) 
 * Updated the icons used in the options dialog
 * Added links to the About dialog
 
## 0.9.7 ##

 * Tidied up code and language files
 * Automatically show the Enter Master Password dialog on startup (if required)
 * Added separators between save types in the submenu
 * Pause form cleanup whilst the context menu is open 
 * Added new pane (Saved forms) to Options dialog 
 * Updated website URLs to http://lazarus.interclue.com/
 
## 0.9.6 ##
 
 * Reworked database to fix "context menu takes too long to show" problem
   when right-clicking on a large form with many saved versions of the form in the database.
 * Added index to database in an attempt to improve context menu speed
 * Speed up form hash computation
 
## 0.9.5 ##
 
 * Disabled "Cleanup on uninstall", as it's not working correctly
 * Added "Set master password" button to options
 * Fixed a wrong icon in install.rdf
 * No longer shows "Master password required" dialog on autosave

## 0.9.4 ##
 
 * Tidied up Options dialog
 * Fixed conflict with Facebook Toolbar 1.2.1
 * Added login menu item if Master Password is required

## 0.9.3 ##
 
 * All form data is now encrypted! 
 * Fixed error where "Clear Private Data Now" button failed to clear Lazaraus saved forms
 * Set limit (10) on for the number of savepoints for each form
 * Option to show time of save rather than text of saved form in submenu
 
## 0.9.2 ##
 
 * Status-bar icon doesn't fit in status bar
 * Version number in status-bar icon tooltip is now correct
 * Added context menu to status-bar icon
 * No longer show disabled "restore form" if it's the only menu item
 * Renamed images 
 
## 0.9.1 ##

 * Much nicer "clear private data" code
 * Show a Lazarus icon in the status bar
 * Added option for "show in status bar" 
 * Added option to clear private data/prefs on uninstall
 * Remove saved forms when clearing private data
 * Let users choose larger values for save form info
 * Only make new autosave point if more then 25% of the text has changed
 * Move prefs code to separate file
 * Toggle units box with time box on options dialog
 * Tidied up sanitize dialog
 * Introdued separate overlays for /preferences/sanitize.xul and /content/sanitize.xul
