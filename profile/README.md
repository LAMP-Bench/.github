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

  - Start / stop Apache, Nginx, MySQL (5.7 ↔ 8.0) and Redis from a sidebar of toggles
  - Virtual hosts with per-host PHP version via `mod_fcgid`
  - Auto-generated local CA + per-host leaf certs — `https://yourapp.local:8443` with a
  green padlock and no `--ignore-certificate-errors`
  - One-click WordPress installs (database, config, host and cert in one go)
  - Composer, Laravel scaffolding, `git init` from the Add Host form
  - Monaco editor for `php.ini` and project files, with one-click `php -l` lint
  - Live tail of Apache / Nginx / MySQL error logs

  ## Status

  Pre-1.0. The code is moving fast and can change shape between commits.
  Bug reports and ideas are welcome via issues — please don't open pull
  requests yet, they'll almost certainly conflict with the next push.

  ## License

  [MIT](https://github.com/LAMP-Bench/lamp/blob/main/LICENSE)
