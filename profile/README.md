# LAMP Bench

A native local web development environment for Windows, macOS and Linux.
Free, open source, no fanfare.

If you've used MAMP PRO, XAMPP or WAMP, you already know the shape of it —
Apache, Nginx, MySQL, multi-version PHP, SSL, phpMyAdmin, all tied together
by a desktop app you start when you sit down to work. LAMP Bench is that,
rebuilt from scratch in Tauri + Rust.

## Projects

- **[lamp](https://github.com/LAMP-Bench/lamp)** — the main app. Tauri
  shell, Rust core, React UI. Everything lives here until something earns
  its own repo.

## What it does

- Start / stop Apache, Nginx, MySQL (5.7 ↔ 8.0), Redis and MailHog from a
  sidebar of toggles — no CMD windows flashing, closes to the system tray
- Per-service config inline: editable listen ports (with collision checks)
  and MySQL version, right from the sidebar
- Virtual hosts with per-host PHP version via `mod_fcgid`
- Auto-generated local CA + per-host leaf certs — `https://yourapp.local:8443`
  with a green padlock and no `--ignore-certificate-errors`. Trusted on
  Windows, macOS and Linux
- One-click WordPress / Joomla / Drupal / MediaWiki (database, config, host
  and cert in one go)
- Versions & components panel: install/remove any runtime, toggle PHP
  extensions, and a one-click ionCube loader installer (picks the build for
  your PHP version — handy for XenForo & co.)
- Composer, Laravel scaffolding, `git init` from the Add Host form
- Monaco editor for `php.ini` and project files, with one-click `php -l` lint
- Per-host snapshots (`.tar.zst`, optional MySQL dump) and FTP deploy with
  saved per-host profiles
- Image optimizer (lossless PNG + JPG re-encode) and a mobile QR code to open
  your site on a phone over the LAN
- Dynamic DNS updates (No-IP / Dyn / DNS-O-Matic / easyDNS / spDYN)
- Live tail of Apache / Nginx / MySQL / Redis / MailHog logs
- Settings with English / Spanish / French, an in-app auto-updater, and a
  single-instance lock so two copies never fight over the same ports

## Install

Grab a build from the rolling
[alpha-testing release](https://github.com/LAMP-Bench/lamp/releases/tag/alpha-testing):
`.exe`/`.msi` (Windows), universal `.dmg` (macOS Intel + Apple Silicon),
`.deb`/`.rpm`/`.AppImage` (Linux). A slim installer downloads the services
on first launch; the app keeps itself updated after that.

> Windows is the most exercised target today. The cross-platform plumbing is
> in place; native Linux/macOS service binaries are still being pinned.

## Status

Pre-1.0, rolling alpha. The code moves fast and can change shape between
commits. Bug reports and ideas are welcome via issues — please don't open
pull requests yet, they'll almost certainly conflict with the next push.

## License

[MIT](https://github.com/LAMP-Bench/lamp/blob/main/LICENSE)
