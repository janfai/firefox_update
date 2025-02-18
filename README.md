# Firefox Auto-Update for Debian GNU/Linux

This script automatically installs and updates Firefox on Debian GNU/Linux systems. It's particularly useful for keeping Firefox up-to-date without manual intervention. The script is based on the original work by raulsaavedr (see Citations section).

## Key Features

- Automatic system architecture detection (32-bit or 64-bit)
- Works for both installation and updates
- Automatic detection of the latest Firefox version
- Logging of the update process
- Removal of old archive versions

## Usage

To run the script manually, use:

```bash
sudo bash /etc/cron.weekly/check_firefox
```

## Script Installation

To install the script on your system, use the following commands:

```bash
sudo wget -O /etc/cron.weekly/check_firefox https://raw.githubusercontent.com/janfai/firefox_update/master/check_firefox
sudo chmod 755 /etc/cron.weekly/check_firefox
```

To change the Firefox language to your preferred language, modify the `language` variable in the script.

## Script Functionality

The script performs the following steps:

1. Checks for and installs sudo and curl if necessary
2. Creates required directories
3. Detects system architecture
4. Determines the latest available Firefox version
5. Compares with the currently installed version
6. Downloads the latest Firefox version if needed
7. Checks the integrity of the downloaded archive
8. Extracts the archive and updates Firefox
9. Removes old archive versions

## Logging

The script logs the update process to `/var/log/firefox_update.log`.

## Automatic Updates

The script is set up in `/etc/cron.weekly/`, ensuring it runs automatically once a week.

## Version Check

The script automatically checks the current version and compares it with the latest available version.

## Recommendations

- Regularly check the log file to verify successful updates
- In case of update issues, you can run the script manually with the `-x` switch for detailed output

This script provides a robust solution for automatic Firefox management on Debian GNU/Linux systems, including installation, updates, and version checks.

### Citations:
[1] https://github.com/raulsaavedr/firefox_update/blob/master/check_firefox

[2] https://github.com/janfai/firefox_update/blob/master/check_firefox

