# ConvertSIDtoAccountName.vbs

Convert an Active Directory SID to an account name with VBScript

## Description

This VBScript script allows you to convert a Windows Security Identifier (SID) to its corresponding account name and domain. It uses Windows Management Instrumentation (WMI) to query the system's account information.

The script prompts the user to enter a SID via an input box, then retrieves and displays the associated user account name and domain name.

## Prerequisites

- Windows operating system with WMI support
- Administrative privileges may be required for certain SIDs
- VBScript execution enabled (default on most Windows systems)

## Usage

1. Download or copy the `ConvertSIDToAccountName.VBS` file to your local machine.
2. Run the script using one of the following methods:
   - Double-click the `.vbs` file (uses WScript by default)
   - Run from command line: `cscript ConvertSIDToAccountName.VBS`
3. When prompted, enter the SID you want to convert.
4. The script will display the account name and domain, or an error message if the SID is invalid or not found.

## Example

Input SID: `S-1-5-21-1234567890-1234567890-1234567890-1001`

Output:
```
User:    JOHNDOE
Domain:  MYDOMAIN
```

## Notes

- The script uses the local machine's WMI service (server = ".").
- Error handling is included for invalid SIDs.
- This script works with local and domain accounts accessible via WMI.
