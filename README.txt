TRANSLUCENT FIREFOX THEME
=========================

A personal CSS theme that makes parts of the Firefox interface and home page
more transparent, with navy blue and gold accents.

FILES
-----

userChrome.css
  Styles the Firefox interface, including toolbars, tabs, the address bar,
  buttons, menus, and panels.

userContent.css
  Styles backgrounds and selected elements on the Firefox New Tab and Home
  pages (about:newtab and about:home).

REQUIREMENTS
------------

Firefox must be configured to load custom stylesheets. The visible
transparency also depends on Windows and its transparency effects. These CSS
files make Firefox surfaces transparent, but cannot make the Windows window
itself transparent on their own.

INSTALLATION
------------

1. In Firefox, open about:support.
2. Next to “Profile Folder”, click “Open Folder”.
3. Fully close Firefox.
4. In the profile folder, create a folder named chrome if it does not already
   exist.
5. Copy userChrome.css and userContent.css from this repository into that
   chrome folder.
6. Reopen Firefox and enter about:config in the address bar.
7. Search for toolkit.legacyUserProfileCustomizations.stylesheets and set its
   value to true.
8. Restart Firefox.

If Firefox does not load the theme, check that the files are in the chrome
folder of the profile you are using, then restart the browser.

UNINSTALLING
------------

Close Firefox, then rename userChrome.css and userContent.css (for example,
to userChrome.css.disabled and userContent.css.disabled). Firefox will stop
loading these styles the next time it starts.

CUSTOMIZATION
-------------

The main interface colors are defined near the top of userChrome.css:

  --glass-ink   navy blue
  --glass-gold  gold accent
  --glass-text  text color
  --glass-muted secondary text color

The home page rules in userContent.css also use these colors directly in CSS
values.

NOTE
----

Firefox updates may change internal interface elements and require the CSS
selectors to be adjusted. Keep a backup of the files before editing them.

Preview
-------

(preview.png)
