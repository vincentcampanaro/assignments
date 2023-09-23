# Sheets to Tasks Assignment Sync

Synchronize your Google Sheets assignments with Google Tasks seamlessly.

## Introduction

This Google Apps Script allows you to automatically synchronize assignments listed in a specific [Google Sheets template](https://docs.google.com/spreadsheets/d/1ALoho_3oHCHn7qsL3HuwOTkCWu2Rz3ZojE3SVflN65c/edit?usp=drive_link) to Google Tasks. Any task added to the sheet is added to Google Tasks if it doesn't already exist there, ensuring you never miss out on a task.

## Features

- 🔄 **Auto-Sync**: The script will check if the task already exists on Google Tasks. If not, it will add the task.
- 🌍 **Timezone Aware**: The script considers your Google account's timezone when creating tasks.
- 🛠 **Customizable Mode**: Switch between "test" mode (no tasks are added to Google Tasks, but logs will show the action) and "active" mode (tasks are added to Google Tasks).

## Prerequisites

- Access to [this assignment template on Google Sheets](https://docs.google.com/spreadsheets/d/1ALoho_3oHCHn7qsL3HuwOTkCWu2Rz3ZojE3SVflN65c/edit?usp=drive_link). It's essential to use this specific template for the script to function correctly.
- Google Apps Script environment to run the provided script.

## Setup

1. **Google Sheets Template**: Start by making a copy of [this assignment template](https://docs.google.com/spreadsheets/d/1ALoho_3oHCHn7qsL3HuwOTkCWu2Rz3ZojE3SVflN65c/edit?usp=drive_link).

2. **Google Apps Script**:
   - Open your Google Sheets template.
   - Click on `Extensions` > `Apps Script`.
   - Delete any code in the script editor and replace with the provided script.
   - Click on the disk icon or `File` > `Save` to save.

3. **Select Mode**: 
   - In the script, change the value of the `MODE` constant to either "test" or "active" depending on your requirement.
     - "test" Mode: This won't create any tasks in Google Tasks, but you'll see logs of the actions.
     - "active" Mode: This will create tasks in Google Tasks based on the assignments in your Google Sheets.

4. **Permissions**:
   - The first time you run the script, you will be prompted to grant permissions. This is necessary for the script to read your Google Sheets data and manage your Google Tasks. Make sure to allow the necessary permissions.

5. **Running the Script**: 
   - Go back to the Google Apps Script environment and run the `createTask` function.

6. **Scheduling (Optional)**:
   - If you wish to run this script automatically at regular intervals, you can set up triggers in the Google Apps Script environment.

## Support

Should you run into any issues or have suggestions for improvements, please file an issue in this GitHub project.

## Conclusion

This script ensures you're always on top of your assignments by seamlessly syncing them with Google Tasks. No more missed tasks or manual data entry required. Just add your assignments to the Google Sheet, and let the script do its magic!
