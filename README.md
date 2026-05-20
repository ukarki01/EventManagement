# EventBoard 🗂️

A free, self-contained event team management app — built as a single HTML file. No account, no subscription, no server. Just open it in a browser and start organizing.

---

## What it is

EventBoard is a lightweight project management tool designed for event organizers and their teams. It works like monday.com or Trello — boards, task groups, statuses, assignees, comments — but lives entirely on your computer as a single `.html` file.

---

## Features

- **Multiple workspaces** — create separate boards for each event (gala, conference, charity run, etc.)
- **Task groups** — organize tasks into color-coded groups within each board
- **Three views**
  - Table — spreadsheet-style list with all task details
  - Kanban — column layout grouped by status (To do / In progress / Done / Stuck)
  - Calendar — tasks organized by due month
- **Task management** — set status, priority, assignee, and due date per task
- **Comments & notes** — post timestamped comments on any task; delete them when resolved
- **Persistent storage** — all data saves automatically to your browser's local storage; your boards are still there when you reopen the file
- **CSV export** — export the current board or all boards to a `.csv` file, ready for Excel or Google Sheets
- **Dark mode** — automatically follows your system preference
- **No install, no login, no internet required**

---

## Getting started

1. Download `eventboard.html`
2. Double-click the file — it opens in any modern browser (Chrome, Firefox, Safari, Edge)
3. Your data saves automatically as you work

That's it.

---

## How to use

### Adding a workspace
Click **+ Add workspace** in the left sidebar. Give it a name (e.g. "Awards Night 2026") and it appears as a new board with its own color.

### Adding tasks
Click the **+ Add task** button in the top bar, or the **+ Add task** link at the bottom of any group. Fill in the task name, group, status, priority, assignee, and due date.

### Editing a task
Click any task row to open its detail panel. From there you can:
- Change the status or priority
- Reassign it to a different team member
- Read and post comments
- Close the panel when done

### Leaving a comment
Open a task, scroll to the Comments section, type your note, select your name from the dropdown, and click **Post comment**. Comments include a timestamp and can be deleted individually.

### Marking tasks complete
Click the checkbox on the left of any task row. It marks the task as Done and strikes through the name. Click again to uncheck.

### Exporting to CSV
- **Export this board** — exports only the currently open workspace
- **Export all boards** — exports every workspace into one file

Both options are available in the top bar and in the left sidebar. The CSV includes: board name, group, task name, status, priority, assignees, due date, completion status, and all comments.

---

## Team members (default)

The app comes pre-loaded with five team member slots:

| Initials | Name |
|----------|------|
| JL | Jamie L. |
| AR | Alex R. |
| TK | Taylor K. |
| MP | Morgan P. |
| SW | Sam W. |

To customize member names, open `eventboard.html` in a text editor and find the `MEMBERS` array near the top of the `<script>` section:

```js
const MEMBERS = ['Jamie L.', 'Alex R.', 'Taylor K.', 'Morgan P.', 'Sam W.'];
```

Replace any name with your team member's name and save the file.

---

## Data & storage

All data is stored in your browser's **localStorage** under the key `eventboard-standalone-v1`. This means:

- Data persists between sessions on the same browser and computer
- Clearing your browser's site data will erase the board — export a CSV backup first if needed
- Data does not sync between devices or browsers automatically; use CSV export/import for that

---

## Customization

Since everything is in one file, you can open `eventboard.html` in any text editor (VS Code, Notepad, TextEdit) and modify:

| What | Where in the file |
|------|-------------------|
| Team member names | `const MEMBERS = [...]` |
| Default board data | `const DEFAULT_BOARDS = [...]` |
| Brand colors | CSS variables in `<style>` (`:root` block) |
| Status labels | `const COLORS = {...}` |
| Priority labels | `const PRIORITY = {...}` |

---

## Sharing with your team

EventBoard is a single file, so sharing is simple:

- **Email** — attach `eventboard.html` and send it
- **USB / shared drive** — copy the file; anyone can open it
- **Host online** — drop the file into [Netlify Drop](https://app.netlify.com/drop), [GitHub Pages](https://pages.github.com/), or [Vercel](https://vercel.com/) for a shareable link

Note: if hosted online, each person's changes save to their own browser — data does not sync between users. For team-wide sync, export and share CSVs, or ask a developer to add a backend.

---

## Requirements

- Any modern browser: Chrome 90+, Firefox 88+, Safari 14+, Edge 90+
- Internet connection on first open (loads the Tabler icon font from a CDN)
- After that, works fully offline

---

## License

Free to use, copy, and modify for personal or organizational use. No attribution required.

---

*Built with plain HTML, CSS, and JavaScript. No frameworks, no build tools, no dependencies.*
