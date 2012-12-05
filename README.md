Light Table Playground
======================

Issues and wiki for the Light Table Playground

#Changes

##0.2.1

* FIX: console.log on uncaught exceptions crashes the app
* FIX: two eval responses coming in at the same time caused a JSON parse error due to the new line separation
* FIX: start clients in the project directory to make sure paths are correct
* FIX: undo will no longer remove the file's content
* FIX: find works from the commandbar and should work with all editors, including the instarepl
* FIX: gracefully handles when the settings file doesn't exist
* FIX: save dialog has more obviously intentioned buttons
* FIX: windows pathing issues that prevented drives other than C:\ from being shown
* FIX: dramatically speed up eval
* FIX: settings were being replaced on each invocation due to a constant re-deploy bug
* FIX: prevent multiple instances of the app from opening, causing address in use issues
* FIX: spurious update messages when off the network
* UPDATE: moved to codemirror v3
* UPDATE: moved to node-webkit 0.3.5
* ADDED: you can now open files from the OS with LT
* ADDED: version command to see change log and version info

##Known issues for 0.2.0
* [mac] Doesn't work on 10.6 until I get a machine to compile it on
* [mac] Untaring updates is really slow due to a chromium event loop bug (doesn't impact editing)
* [linux] Frameless windows aren't resizable, so it is framed. Blocked by [chromium bug](http://code.google.com/p/chromium/issues/detail?id=156465)
* [win] Child processes bring up a command prompt that steals focus. Will be fixed with next shell release.
* [win] As a result of the above, java connection processes can sometimes live on after the app is closed.
* [all] No context menus - waiting to see what the impact of this is.