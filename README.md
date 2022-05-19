# mptr-jira

For Microsoft Powertoys Run, Open Jira tickets based on ticket number.

## Usage

### Opening a ticket with the default ticket prefix

`jira 123`

### Opening a specific ticket

`jira TICKET-123`

### Searching

`jira my search query`

## Installation

Installation can be performed in different, manual, ways:

Default Power Toys installation dir is `%PROGRAMFILES%\PowerToys`.

**Easy (for most users):**
Copy files to plugin folder

1. Make sure Power Toys is not running.
2. Copy files to your Power Toys Run plugin folder (`[...]\PowerToys\modules\launcher\Plugins`).
3. Start Power Toys.
4. ???
5. Profit!

**Harder (for developers that intend to change code):**
Create symlink in your Power Toys Run plugin folder.

1. Launch cmd as an administrator, and navigate to `[...]\PowerToys\modules\launcher\Plugins`.
2. Create symlink with: `mklink /D mptr-jira DESTINATION`, where `DESTINATION` is the binary output folder where your Visual Studio compiles this code (example: `C:\git\mptr-jira\mptr-jira\bin\Release\net6.0-windows`)
3. Build project (the Visual Studio project is configured to kill PowerToys.exe before build, and re-launch after).
3. ???
4. Profit

## Settings File

`UrlPrefix` is the URL to your JIRA server. It must end with a slash character (`/`).

`DefaultTicketPrefix`

```
{
  "UrlPrefix": "https://my-jira-server.internal/",
  "DefaultTicketPrefix": "TICKETNAME"
}
```

## Usage of Atlassian Jira name and icon.
This project is in no way associated with Jira, Jira Software or Atlassian. If you make changes to this project, make sure you follow Atlassian terms and guidelines how to user their logo and name.
Usage of Jira name and logo/icon in this Power Toys Run plugin (mptr-jira) follows guidelines described in:
- https://www.atlassian.com/legal/trademark (2022-05-19).
- https://www.atlassian.com/company/news/press-kit (2022-05-19)