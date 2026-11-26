# Board

A simple personal Kanban board for Windows, with a lunch break timer.

- Four columns: To Do, In Progress, Done and In Production. Rename any of them (for example, In Production to Archive) by hovering the column name and clicking the pencil.
- Drag cards between columns, search with `/`, and add a card with `N`.
- **On break** tab: press **Go on lunch** (or `L`) for a one-hour countdown. When it's up, Board chimes and shows a Windows notification.
- Everything is saved on your own PC. Nothing is sent anywhere.

This repository holds Board's releases. Download the installer from the [latest release](https://github.com/mortillerogino/personal-kanban/releases/latest).

## Install

You need 64-bit Windows 10 or 11. You don't need admin rights.

1. Open the [latest release](https://github.com/mortillerogino/personal-kanban/releases/latest) and, under **Assets**, click **KanbanToDo-win-Setup.exe** to download it.
2. If your browser says the file "isn't commonly downloaded", keep it: click the **...** next to the download and choose **Keep** (in Edge, then **Show more** > **Keep anyway**). This happens because the installer is new and isn't code-signed.
3. Double-click **KanbanToDo-win-Setup.exe**. Windows may show a blue "Windows protected your PC" message. Click **More info**, then **Run anyway**. You only see this the first time.
4. Board installs in a few seconds and opens. It adds a **Board** shortcut to your desktop and Start menu.

To get the lunch-over alert, keep Windows notifications on (**Settings** > **System** > **Notifications**). With Do not disturb on, the alert won't pop up, but the chime and the red timer still show it.

## Updates

Board keeps itself up to date. Every few hours it checks for a new version and downloads it in the background. The update installs the next time you close Board, or straight away if you click **Restart now** in the update message.

## Your data

Your board is saved in `%APPDATA%\KanbanToDo` on your PC (paste that into File Explorer's address bar to open it):

| File or folder | What it is |
| --- | --- |
| `board.db` | Your cards, lunch breaks and column names |
| `Backups` | Automatic copies taken before an update changes your board (the last 10 are kept) |
| `error.log` | Details of any errors, if something goes wrong |

Updating or uninstalling Board never touches this folder. To move your board to another PC, close Board and copy `board.db` into the same folder there.

## Uninstall

Go to **Settings** > **Apps** > **Installed apps**, find **Board**, and choose **Uninstall**. Your board stays in `%APPDATA%\KanbanToDo`, so reinstalling brings it straight back. To remove it completely, delete that folder too.

## Troubleshooting

- **Setup won't run, or says it's blocked by your organisation:** on a work PC, IT policy may stop apps that aren't code-signed. Your IT team would need to allow it.
- **"Board needs the Microsoft Edge WebView2 Runtime":** this comes with Windows 10 and 11 but can be missing. Install it from [Microsoft](https://go.microsoft.com/fwlink/p/?LinkId=2124703), then open Board again.
- **Board won't open or shows an error:** check `%APPDATA%\KanbanToDo\error.log` and send it to whoever gave you Board.

## Keyboard shortcuts

| Key | Does |
| --- | --- |
| `N` | Add a card to To Do |
| `/` | Search |
| `L` | Go on lunch, or time in |
| `Esc` | Close the card drawer or menu, or cancel renaming a column |
