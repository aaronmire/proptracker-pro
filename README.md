# PropTracker Pro - Changelog

----- <b><i>v1.1</b></i> -----
- Added Calendar
- Added selection buttons in Evaluation Accounts and Payout Logs
- Updated JSON export file names
- Updated icon and colors
- Made second row (Evaluation Accounts, Payout Logs, etc.) sticky for quicker access if scrolled down on a page

----- <b><i>v2.0</b></i> -----
- Added Google Cloud syncing
- Added settings menu:
  - Import/Export manual backups
  - Choose folder where to sync on Google Drive 
- UI updates

----- <b><i>v2.1</b></i> -----
- Updated UI
  - Changed settings menu to hamburger menu
  - Moved Tax Report to new menu
  - Updated Google sync and syncing indicator to help with mobile visualization
 
----- <b><i>v2.2</b></i> -----
- Modal popups when editing entries on Evaluation Accounts and Payout Logs tabs
- Manual cloud sync button added
- Rename Dashboard Overview to Dashboard
- Replaced calendar month/year picker with a popup modal
- Modernized Google Drive folder picker
- Moved Google account connection to the settings menu 

----- <b><i>v2.3</b></i> -----
- Cloud upload changes - clicking it forces immediate write to proptracker_data.json with latest workspace changes
- Account size/type formatting
- Added persistent Google Sign-In token to stay signed in with Google when reloading app

----- <b><i>v3.0</b></i> -----
- New Journal tab

----- <b><i>v3.1</b></i> -----
- Added Pull-Before-Push method so JSON files pull from Google Drive and no longer overwrites on auth
  - Blocks premature writes and debounces sync triggers on login until cloud data is fetched and verified
  - When syncing between devices, evaluations, payouts, and journal entries are combined by unique id, and ties/updates are resolved using an explicit lastModified timestamp on every object
  - Mobile logins will pull the laptop's newer entries from Google Drive rather than pushing stale localStorage over the cloud file
