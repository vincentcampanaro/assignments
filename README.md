# Sheets to Tasks Assignment Sync
Synchronize your Google Sheets assignments with Google Tasks seamlessly.

## Introduction
This Google Apps Script synchronizes assignments listed in a specific Google Sheets template to Google Tasks. Any task added to the sheet will be automatically added to Google Tasks based on the mode set in the script.

## Features
- **🔄 Auto-Sync**: If the task doesn't already exist on Google Tasks, it's added.
- **🌍 Timezone Aware**: The script respects your Google account's timezone when creating tasks.
- **🛠 Modes**: There are three modes you can use:
  - "test": Logs actions but doesn't add or delete tasks on Google Tasks.
  - "active" (work in progress): Adds and updates tasks based on the Google Sheets data.
  - "manual": Deletes all existing tasks and creates them from scratch based on the Google Sheets data.

## Prerequisites
- [Assignment template on Google Sheets](https://docs.google.com/spreadsheets/d/1ALoho_3oHCHn7qsL3HuwOTkCWu2Rz3ZojE3SVflN65c/edit?usp=drive_link). **You must use this specific template for the script to function correctly.**
- Google Apps Script environment to run the script.

## Setup

### Google Sheets Template:
1. Make a copy of the [assignment template](https://docs.google.com/spreadsheets/d/1ALoho_3oHCHn7qsL3HuwOTkCWu2Rz3ZojE3SVflN65c/edit?usp=drive_link).

### Google Apps Script:
2. Open your copied Google Sheets template.
3. Navigate to `Extensions` > `Apps Script`.
4. Erase any existing code in the script editor and paste in the provided script.
5. Save your changes.

### Select Mode:
6. In the script, adjust the value of the `MODE` constant to your desired mode: "test", "active", or "manual".

### Permissions:
7. The first time you execute the script, it will request permissions. Grant them to enable the script to read your Google Sheets data and handle your Google Tasks.

### Running the Script:
8. Go back to the Google Apps Script environment.
9. Execute the `createTask` function.

### Automatic Synchronization on Edit (Optional):
You can set up the script to run automatically when you make an edit to the Google Sheet.

1. In the Google Apps Script environment, click on the left sidebar's clock icon to access triggers.
2. Click on `+ Add Trigger` at the bottom-right.
3. For the function to run, select `createTask`.
4. For the event source, select `From form` > `On edit`.
5. Save the trigger. Now, whenever you edit the Google Sheet, the script will run.

## Support
For issues or suggestions, please open an issue in this GitHub repository.

## Conclusion
Stay on top of your assignments by syncing them with Google Tasks automatically. Just populate your assignments in the Google Sheet and let the script handle the rest!
