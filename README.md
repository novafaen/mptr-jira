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
Assumption: Power Toys is installed in <pre>%PROGRAMFILES%\PowerToys</pre>, otherwise update installation paths with your paths.

Easy (for most users): Copy files to plugin folder

1. Make sure Power Toys is not running.
2. Copy files to your Power Toys Run plugin folder (<pre>[...]\PowerToys\modules\launcher\Plugins</pre>).
3. Start Power Toys.
4. ???
5. Profit!

Harder (for developers that intend to change code): Create symlink in your Power Toys Run plugin folder.

1. Launch cmd as an administrator, and navigate to <pre>[...]\PowerToys\modules\launcher\Plugins</pre>.
2. Create symlink with: <pre>mklink /D mptr-jira DESTINATION</pre>, where <pre>DESTINATION</pre> is the binary output folder where your Visual Studio compiles this code (example: <pre>C:\git\mptr-jira\mptr-jira\bin\Release\net6.0-windows</pre>)
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
