# MDAntiCheat: issues and suggestions

This is where server owners report problems with **MDAntiCheat** and suggest new features. The
plugin's code isn't here; this repository only holds issues.

MDAntiCheat is a physics-based anticheat for **Paper and Spigot 1.16.5 – 26.3**. Instead of fixed
speed limits, it predicts what vanilla movement allows on every tick, so it catches cheaters
without flagging your players.

## Open an issue

Go to **[Issues → New issue](../../issues/new/choose)** and pick a form:

| Form | Use it when |
|---|---|
| **False positive** | A legit player gets flagged, set back or punished |
| **Bug report** | Something is broken: an error, a crash, a command or setting that doesn't work |
| **Undetected cheat** | A cheat client or module gets past the anticheat |
| **Suggestion** | You'd like a new feature, a new check or an improvement |
| **Question** | You want to know how something works or how to set it up |

Before you open one, please search the [existing issues](../../issues?q=is%3Aissue) — if yours is
already there, add a 👍 or a comment with your details instead of a new issue.

## What to include

The forms ask for these, and they make the difference between a quick fix and a long back-and-forth:

- **Versions:** MDAntiCheat, your server (e.g. `Paper 1.21.4-232`) and PacketEvents. `/version AntiCheat`
  and `/version` show them.
- **The alert:** for a false positive, run `/ac logs <player>` and paste the rows. The details in
  brackets show what was measured and the limit.
- **What the player was doing:** the more specific, the better ("sprint-jumping up stairs while
  eating", not "walking").
- **Other plugins** that move players or change combat: launch pads, grappling hooks, custom
  knockback, vehicles, minigames.
- **For a bypass:** the cheat client, the module and its settings. A short video helps a lot.
  Please don't post download links to cheat clients.

## What happens next

Every new issue starts with the `needs-triage` label. After it's been looked at, its labels show
where it stands:

| Label | Meaning |
|---|---|
| `needs-info` | We need more details from you; the issue waits for your reply |
| `confirmed` | Reproduced; it will be fixed |
| `planned` | Suggestion accepted and on the roadmap |
| `in progress` | Being worked on |
| `fixed in next release` | Done; it ships in the next update |
| `duplicate`, `not a bug`, `wontfix` | Closed, with a comment explaining why |

Issues are also labelled by type (`bug`, `false-positive`, `bypass`, `suggestion`, `question`),
by area (`area: movement`, `area: combat`, ...), by platform (`platform: paper`,
`platform: spigot`) and by priority.

## Security problems

If you find a way to crash a server or harm players through the plugin, please don't post the
details publicly. Open a **Bug report** saying only that you found a security problem, and you'll
be contacted privately for the details.

## For maintainers

- **Labels** live in [`.github/labels.json`](.github/labels.json). Edit that file on `main`, and
  the **Sync labels** workflow creates or updates them. It never deletes labels.
- **Project board:** the **Add to project** workflow puts every new issue on the Blocksmith project
  board, next to the plugin's own issues. It needs a repository secret `PROJECT_TOKEN`: a classic
  personal access token with the `project` and `repo` scopes. The board defaults to
  `https://github.com/users/Vasilew69/projects/1`; set a repository variable `PROJECT_URL` if
  yours is different. Run it manually (Actions → Add to project → Run workflow) to add every open
  issue.
