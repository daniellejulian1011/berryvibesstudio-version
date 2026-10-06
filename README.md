# Berry Vibes Studio × CCD — V5.4

Multi-page HTML/CSS/JavaScript website for GitHub Pages, with an optional Node backend for server authentication, uploads and log sync.

## V5.4 changes
- Removed the Social page.
- Removed the About page.
- Removed the standalone Account page and the old Profile redirect.
- Merged account/profile controls into `settings.html`:
  - profile photo
  - display name
  - height in feet/inches (for example `5'2`)
  - weight
  - reason for using the website
  - sign-in status
  - sign out
  - full website themes
  - motion/gallery settings
  - daily recipe recommendations
  - default start page
  - export/import and reset tools
- Signed-in navigation now sends the top-right account/settings control to `settings.html`.
- Hamburger navigation no longer contains Social, About, Account or Profile links.

## Fasting behavior
The Fasting page now records both sides of a fast.

### Start after last meal
`START FAST AFTER MY LAST MEAL`:
1. Finds the latest timed Food, SOTD/snack or Restaurant log on the selected day.
2. Uses that meal time as the fasting start.
3. Immediately creates a **FAST START** log.
4. Saves the fast as the active fast so it survives a page reload in the same browser.

Manual `START + LOG FAST` does the same thing using the time wheel.

### Break fast
`BREAK + LOG FAST`:
1. Uses the selected break date + time.
2. Calculates the elapsed fasting time from the active start.
3. Creates a separate **FAST BREAK** / completed fast log.
4. Marks the original start log complete and clears the active fast.

The Fast History shows both start and break records. The Calendar recognizes fast-start entries as fasting activity.

## Current pages
- Today
- Food
- Recipes
- SOTD
- Move
- Fasting
- Restaurants
- Grocery
- Food Battle
- Facts
- Calendar
- Period Tracker
- Settings + Account
- Sign In
- Sign Up
- Forgot Password
- Forgot Username
- Reset Password

## Deployment
Upload all files/folders in this package to the repository root. Delete obsolete `social.html`, `about.html`, `account.html`, and `profile.html` from the GitHub repository if they still exist from an older version.

For GitHub Pages, browser-local accounts and data work without a server. Deploy the included Node backend separately if you want server-side account/log syncing and uploaded-file hosting.
