# AdGuard DNS SDE Demo Extension

> **This repository has moved to GitHub.**
>
> The project is now maintained at [AdguardTeam/dns-sde-extension][new-repo].
> Please use GitHub for the latest code, issues, and pull requests.

[new-repo]: https://github.com/AdguardTeam/dns-sde-extension

This browser extension demonstrates how Structured DNS errors can work if supported natively by browsers.
It listens for web requests and identifies loading errors on main frames.
When an error is detected, it queries the AdGuard DNS DoH (DNS-over-HTTPS) service
with structured DNS errors enabled to check if the page was blocked.

If AdGuard DNS has blocked the page, the extension displays a custom block page
with detailed information about the block.

## How to use

1. Go to `chrome://extensions/`.
1. Enable developer mode.
1. Install the extension from `src` directory by clicking `Load unpacked`.
1. The extension options page will open.
1. Set the AdGuard DNS custom server due to the instructions on the options page.

> **Note:** No other DNS should be set on the system level or in your network settings.

## Permissions required

- `webRequest` - necessary for detecting tab loading errors.
