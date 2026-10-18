---
title: Report a problem
description: What to include and where to post when DesignZ misbehaves or crashes.
order: 20
verified: 0.7.1
---

Post in the [issue tracker](https://github.com/danish0440/designz/issues) or in [Discord](https://github.com/danish0440/designz/issues), and attach the log file. The log is the most useful thing you can send after a crash.

## What to include

- Your DesignZ version and how you installed it (installer, portable, AppImage and so on).
- Your operating system and graphics card.
- What you did, what you expected and what happened.
- The log file `designz.log`.

## Where the log is

DesignZ writes `logs/designz.log` in its settings folder, beside `ui.json` and `prefs.json`.

| System  | Log folder                                                              |
|---------|-------------------------------------------------------------------------|
| Windows | `%APPDATA%\DesignZ\logs\`                                           |
| macOS   | `~/Library/Application Support/DesignZ/logs/`                       |
| Linux   | `~/.config/designz/logs/` (or `$XDG_CONFIG_HOME/designz/logs/`) |

Each start moves the previous log to `designz.1.log`, and that one to `designz.2.log`. The log from a run that crashed survives the next start, so attach `designz.1.log` if you have restarted since. The file stops growing at 16 MiB.

## More detail in the log

Set the environment variable `RUST_LOG` to `debug` before starting DesignZ to log more. The default is `info` for DesignZ's own parts and `warn` for everything else.
